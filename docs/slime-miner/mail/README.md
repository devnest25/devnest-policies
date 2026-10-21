# Slime Miner free event mail

Source: `docs/slime-miner/mail/feed.json`
Public HTTPS: https://devnest25.github.io/devnest-policies/slime-miner/mail/feed.json

Initial publication is an empty valid list. Publish real titles, amounts and periods only after the operator specifies them. Synthetic mail belongs only in isolated game verification fixtures.

Schema 1: `schema_version: 1`, `items: []`. Each item has `id`, `starts_at`, `expires_at`, `content: {ko: {title, body}, en: {title, body}}`, `reward: {currency, amount}`. Both languages are required. Times must be valid UTC `YYYY-MM-DDTHH:MM:SSZ` (1970 or later), with starts_at < expires_at. Claims use starts_at <= device time < expires_at.

IDs: 1–64 ASCII letters/digits/underscore/hyphen, globally unique, permanently never reused. Changing a published reward or period requires a NEW ID. Retain a publication history in Git and check it before choosing IDs. Removing a mail never removes local claim history.

Currency is `minerals` or `ether` only. Amount is a positive canonical decimal integer STRING (no leading zero, sign, spaces, decimal point or exponent), max36 digits (keeps the full reward notification usable together with the mailbox on small screens). The existing game LargeNumber normalized coefficient and full decimal display must roundtrip without loss; unrepresentable amounts reject the entire feed. Do not pass full amounts through JSON numbers, int or float. Test amounts with the PRODUCT parser before publishing.

Max100 items, 262144 UTF-8 bytes, title1–160 characters and body1–12000, nonblank. Body is plain text; no remote markup is executed. The entire response is rejected for any invalid entry, duplicate ID, invalid schema/period/currency/amount/language or exceeded bound.

1. Edit only this feed on a dedicated branch. Check the full Git history for reused IDs and reward/period mutation. Do not modify `updates/latest.json`.
2. Validate JSON and the current product `EventMailFeed.from_body` parser. Exercise UI/reward cases with isolated fixtures, never public test rewards.
3. Create and merge a PR to main. Existing Pages publishes main `/docs`. Confirm the deployment succeeds.
4. Confirm anonymous HTTPS200 and exact body, then run product `tools/verification/mvp114_public_https.gd`. Record source commit, deployment and verification time. Cached older responses may last around10 minutes (current Pages max-age600); request no-cache is not an immediate purge guarantee.
5. Roll back mistakes through a PR restoring a verified empty/last safe list. Do not reuse IDs or mutate already published rewards/periods; a replacement uses a new ID. A rollback may make a previously published item available again to clients that have not claimed it, so inspect the target content before rollback.

Every open/refresh fetches asynchronously; failures keep the previous list but block new claims until a successful fetch. A previously fetched valid list can still be claimed without a new request until expiry. Removing mail cannot revoke it instantly from all clients, and granted rewards are not clawed back. There is no server ledger/time/authentication. Device clock changes, reinstall, other devices and old local/cloud restores may permit repeat claims under the approved free event policy. No paid products, personal mail, first-come allocation or cross-device duplicate prevention.

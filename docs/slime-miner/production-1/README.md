# Production generation 1

The 2.0.0 production app reads only this namespace and requires `data_generation: "production-1"` in every feed. Mail, coupons, and notices start empty. Existing test notices and patch notes remain in the historical namespace and Git history; they are not served to the production app.

Test mail and coupons have been removed from the old feeds. Retired IDs must never be reused:

- `mail-20261022-test-thanks`
- `mail-20261027-test-thanks-10000`
- `coupon-20261022-devnest` (code `DEVNEST`)

Production content uses new `prod1-` IDs. After launch, retire rewards without deleting local claim history. Keep all historical Git/release evidence.

Launch notice `prod1-launch-200`, patch note `prod1-patch-200-code36`, and update guidance remain drafts in the private game repository. Publish only after the owner confirms the 2.0.0 Play rollout and install availability. Do not create `production-1/updates/latest.json` before that confirmation. A missing endpoint fails closed; there is no fallback to test content.

For the approved rollout, publish the prepared notice/patch JSON with the confirmed publication date and the update manifest `{ "schema_version": 1, "data_generation": "production-1", "latest_version_code": 36, "latest_version_name": "2.0.0" }`. Update the legacy app's version guidance only at that time. Verify Pages deployment and anonymous HTTPS responses before reporting publication complete.

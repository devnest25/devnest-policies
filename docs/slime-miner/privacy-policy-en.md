---
layout: default
title: Slime Miner Privacy Policy
lang: en
---
# Slime Miner Privacy Policy

English · [한국어](privacy-policy.html)

Effective and last updated: **3 November 2026**

**DevNest** (“the Developer”) explains how information is handled in **Slime Miner**, Android package `com.devnest.slimeminer`, including production and test releases. The game does not offer a separate DevNest account or use a developer-operated game backend. However, Google's advertising, billing and gaming services and requests for public operational information on GitHub Pages involve online processing, separate from local device storage.

This policy explains data handling. Reading it, installing the game or continuing to play is not treated as consent to optional personal-data processing. Required advertising consent and changes to privacy choices are handled through the relevant privacy-choice screens.

## 1. Information and purposes

| Category | Information | Location and purpose |
| --- | --- | --- |
| Progress and preferences | Mines, unlocks, ascension, currencies, upgrades, research, slimes, skins, activation, quests, achievements, relics, dungeons, expeditions, language, display and audio settings | Local storage for gameplay and recovery |
| Reward state | Offline timestamps and rewards, ad-reward request identifiers, grant/claim timestamps and state, fractional remainders, free-reward state, claimed event-mail and coupon identifiers | Local calculation, recovery and duplicate-grant prevention. Reward request identifiers are not advertising IDs |
| Play Games connection and ranking | Player ID, display name, connection state, highest unlocked normal-mine stage, record-owner account identifier; player IDs, display names, ranks and highest stages returned by public leaderboard queries | Account checks, score submission to Google Play Games, leaderboard retrieval and display. Your own best record and owner identifier are also stored in local progress |
| Optional cloud saves | Progress, preferences and reward state above, your own ranking record and owner identifier, save format version, save name, description and modification metadata | Google Play Games Saved Games for user-requested manual backup and restore. Retrieved lists of other players are not part of the gameplay save |
| Purchases | Product IDs, purchase tokens, transaction/order details and timestamps returned by Google Play, signed purchase data, purchase/acknowledgement and entitlement state | Google Play billing, verification, acknowledgement and restoration; local purchase journal/cache |
| Public operational information requests | IP address and connection information such as the requested path when fetching update information, notices, patch notes, event-mail/coupon lists or policy pages | Public-file delivery and hosting security on GitHub Pages. The app does not attach gameplay progress, purchase tokens, Play Games IDs or entered coupon codes to these requests |
| Support | Email address, message and diagnostic materials voluntarily supplied | Email support, troubleshooting and rights requests |

The purchase journal containing purchase tokens and signed receipts is separate from the gameplay save and is not included in the game's Play Games backup. Legacy unlock or benefit-migration state in a gameplay save is not proof of a Play purchase.

## 2. Advertising and consent

The game uses Google AdMob (Google Mobile Ads SDK) for rewarded ads. For advertising, measurement, analytics and fraud prevention, Google's SDK may collect and share IP addresses and approximate location, app launches and ad interactions, app/SDK diagnostics, Android advertising IDs, app set IDs and applicable device/account identifiers. Processing varies with SDK version, device, region, consent and ad settings.

Google's User Messaging Platform (UMP) checks and manages privacy choices. Applicable users receive consent, refusal and preference-management options. Where the SDK requires a privacy options entry point, the game's ad privacy setting lets users revisit their choices. Withdrawal affects subsequent processing; it does not automatically erase all previously processed data. Android's ad settings also provide advertising-ID controls.

- **European Economic Area (EEA), United Kingdom and Switzerland:** Where advertising consent is required, Google's UMP provides the notice and choice screens. Refusing or withdrawing required consent can change whether ads are available and which types are served. Local gameplay itself does not require advertising consent.
- **United States and other regions:** Applicable law may provide rights to opt out of targeted advertising or the sale or sharing of personal information. You can use the regional ad-privacy options that are available and Google's privacy controls. Contact us below if you cannot find a choice screen or need help with a request. Message types and availability depend on region, account and advertising-service configuration.

Declining personalized ads does not eliminate all processing needed for ad delivery, security or fraud prevention. Watching ads, advertising consent, connecting Play Games and requesting a manual cloud save are separate choices.

Not watching ads or owning ad removal does not by itself guarantee that all SDK initialization, consent checking or ad-preparation processing stops. The Developer does not operate a separate advertising-tracking or independent analytics server.

[Google Privacy Policy](https://policies.google.com/privacy?hl=en) · [Google partner-service information use](https://policies.google.com/technologies/partner-sites?hl=en) · [Ad SDK disclosures](https://developers.google.com/admob/android/next-gen/privacy/play-data-disclosure)

## 3. Play Games, leaderboards and cloud saves

Local play does not require connecting Play Games. Settings provide connection/status checks and manual cloud save/load. The app uses the player ID to verify account consistency and the display name for connection status and leaderboards. Your ranking record includes its owner's player ID, which is retained in local saves, recovery backups and user-requested cloud saves. The player ID is therefore not used only in memory. It is not sent to a developer-operated backend.

The app does not separately request and store your account email, friends list or profile photo. Google's own authentication, profile, usage and diagnostic processing follows its policies. SDK authentication behavior arising from Google/device settings, leaderboard submission and gameplay-save uploads are separate operations.

### Leaderboard submissions and visibility

While Play Games is connected, the game submits the highest unlocked normal-mine stage, covering the Element and Mineral realms, to the connected account's Google Play Games leaderboard. Submission can occur on connection, when a new best record is saved and on retries. **A record can be submitted without opening the leaderboard or pressing the manual cloud-save button.** The record's owner is checked to avoid submitting it to the wrong account.

The public leaderboard displays the names, ranks and highest stages that Google makes available for public viewing. The app may also retrieve player IDs for list display, duplicate handling and identifying your own entry. Lists of other players are handled in the interface and runtime memory, not added to the normal gameplay save. Visibility follows Google Play Games profile settings and service policies. Manage visibility through Google Play Games profile and privacy settings.

### Manual cloud saves

Manual backup transmits recovery data and save metadata to Google Saved Games, including your best ranking record, its owner identifier and claimed event-mail/coupon state. The gameplay payload excludes support messages, advertising IDs, OAuth authentication tokens, the separate purchase journal and lists of other players. **Saved Games progress backups** are not periodically uploaded without a manual request; a requested save may synchronize later through Google's SDK when connectivity permits. This is distinct from automatic leaderboard submission described above.

[Play Games data disclosures](https://developer.android.com/games/pgs/data-collection) · [Leaderboards and visibility](https://developer.android.com/games/pgs/leaderboards) · [Saved Games](https://developer.android.com/games/pgs/savedgames)

## 4. In-app purchases

Permanent products, including ad removal, Ether Slime and bundles, use Google Play Billing. The app does not directly ask for or store card numbers, bank account numbers or payment passwords. Payment methods are processed under Google Play's and the payment provider's policies.

Purchase information verifies, acknowledges and restores entitlements. Query results reflect entitlement changes such as refunds or cancellations; the last verified state may be cached offline. Your Play purchase account may differ from your Play Games account. Deleting progress does not cancel a purchase or request a refund.

[Google Play Terms](https://play.google.com/about/play-terms/) · [Google Privacy Policy](https://policies.google.com/privacy?hl=en)

## 5. Retention and deletion

- **Local saves, recovery backups and purchase caches:** Retained in app storage for gameplay and recovery. Use Android Settings → Apps → Slime Miner → Storage → Clear data to remove this device's app data; labels vary. Manage any separate operating-system backups through the relevant backup settings.
- **Cloud and leaderboard data:** Use the per-game deletion controls in your Play Games profile; see [Google's deletion instructions](https://support.google.com/googleplay/answer/9130646?hl=en). Clearing local data, uninstalling, changing accounts or making a profile private is distinct from deleting cloud or leaderboard records. If local progress remains after deleting Google-held data, a later manual backup or leaderboard submission while connected may recreate records. Manage both local data and Google's per-game data to avoid recreating them. Google's policies and procedures govern the scope and timing of deletion.
- **Play transactions and ad/authentication data:** Google and payment providers retain these under their policies and legal duties. The Developer cannot directly erase Google's transaction ledger or advertising data. A local purchase cache may be rebuilt after clearing app data by querying valid purchases.
- **Public-file access logs:** Logs handled by GitHub for hosting security and related purposes follow GitHub's retention and privacy-request procedures. Deleting app data does not delete GitHub's access logs.
- **Support materials:** Retained while resolving the request and necessary follow-up, then unnecessary materials are deleted. Any retention needed for disputes or legal obligations is limited to the relevant purpose, scope and necessary period. You may request deletion by email.

Deletion, restriction or consent withdrawal may affect recovery or online features. These actions do not retroactively cancel completed processing or legally required transaction retention.

## 6. External services, international processing and security

Google AdMob/UMP handles ads and consent; Google Play Games handles authentication, leaderboards and cloud saves; Google Play and your payment provider handle billing. Support email is delivered and retained through the Developer's Gmail service. Google may process/share information with service providers and ad partners as described in its policies. Information may be processed outside your country, including in the United States, on Google/service-provider infrastructure. See [Google's international transfer safeguards](https://policies.google.com/privacy/frameworks?hl=en) and Privacy Policy for recipients, locations, safeguards and retention information.

### Public operational files and GitHub Pages

Update information, notices, patch notes, event-mail/coupon lists and these policy pages are hosted on GitHub Pages. The app fetches common public files over HTTPS without attaching Play Games IDs, advertising IDs, purchase tokens, gameplay saves or entered coupon codes. Coupon matching and event-mail/coupon claims are handled on the device. In-game event mail is not an email service addressed to your email account.

However, file requests and page visits involve IP addresses and connection information such as the requested path. GitHub states that it logs Pages visitors' IP addresses for security. This information may be processed outside your country, including in the United States. See the [GitHub Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement) and [Pages data-collection notice](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages#data-collection) for hosting-provider retention, safeguards and privacy requests.

The Developer does not receive the above data on its own game backend; materials you voluntarily email to support are an exception. The absence of a developer-operated backend does not mean there is no online processing by Google or GitHub. Google describes TLS encryption for its ad SDK and HTTPS for Play Games data in transit. Local game storage is not represented as a separately encrypted vault. The Developer does not directly sell personal information. However, advertising partners' processing may be classified as sale, sharing or targeted advertising under applicable law; where applicable, use the ad-privacy choices in section 2 and the rights-request routes below.

## 7. Your rights and children's privacy inquiries

Depending on applicable law, you may request access, correction, deletion, restriction, objection to processing, data portability or withdrawal of consent. Applicable US state laws may also provide rights to opt out of sale, sharing or targeted advertising, appeal a denied request and avoid unlawful discrimination for exercising privacy rights. Where you have a right to complain to a data-protection authority, you may contact that authority.

Email us below for requests concerning information handled by the Developer, such as support materials. We verify the request and its scope only as necessary and respond under applicable legal time limits and procedures. If we cannot carry out a request or another service's process is needed, we explain the reason and available route. For Google- or GitHub-managed information, also use the relevant account, Play Games, ad or privacy-request controls. The Developer cannot remotely access or erase device-only data and does not delete your entire Google account on your behalf.

Parents or guardians may contact us about children's information. Google account/age restrictions and parental controls follow the relevant service settings. Do not send payment passwords, card numbers or authentication tokens to support.

## 8. Contact

- Operator and privacy contact: **DevNest**
- Email: [devnest25@gmail.com](mailto:devnest25@gmail.com)

We may verify the information concerned and your identity or representative authority as necessary to handle a request.

## 9. Changes and languages

We update the effective/last-updated date when processing changes and provide additional app/store notices where appropriate. This English version describes the same processing as the [Korean version](privacy-policy.html); both versions are maintained together.


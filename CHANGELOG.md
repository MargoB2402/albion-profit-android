# Android release notes

## Android 0.9.2 beta - 2026-10-25

Android 0.9.2 beta improves built-in VPN API routing and gathering identification.

- With an imported WireGuard, AmneziaWG or OpenVPN profile, Albion traffic and this app's website/API requests use the built-in tunnel. The tunnel's outer sockets are protected from routing loops; other apps keep normal networking.
- Account verification runs after the built-in tunnel starts. Price uploads wait for successful verification and respect server-enforced private mode.
- Gathering accepts signed character IDs and validated complete zone-entry responses. The free gathering tab shows when character identification or game capture is missing, with seven-language instructions and aggregate counters.

Update by installing the APK over the previous beta; the signing identity and local settings are preserved. A real provider/server profile is required. An external Happ VPN alone does not enable capture: Android tools-only mode is still separate. Existing subscription gates remain unchanged.

Checks: encrypted WG/AWG game/TCP packet roundtrips, Go race tests, four native ABIs, JNI/R8, post-obfuscation JVM regressions, protected UI and narrow-screen checks. There is no connected physical phone; provider-specific Android connectivity and the reported live gathering issue are not yet confirmed. Missing earlier harvest is not reconstructed.

APK, matching native source archive and SHA256SUMS.txt are attached. Private Java/UI sources, credentials and obfuscation mappings are not published.


## 0.9.1 - 2026-10-25

- Added detailed automatic market capture counters and unresolved-market categories, without packet contents or credentials.
- Distinguished Android VPN revocation and reset diagnostic counters between capture runs.
- Preserved signing, Java/WebView hardening and existing gathering/fishing/loot features.
- Diagnostic update: no confirmed Happ fix or new Happ profile support is claimed. Requires the updated website diagnostic sanitizer.

## 0.9.0 - 2026-10-24

- Free Gathering & fishing tab: separate local sessions, grouped resources/fish and expandable time/location/quantity history.
- Compare seven cities for instant sale or sell orders, with configurable fees, freshness and best cities per item/whole harvest.
- Preserved Java/WebView obfuscation, signing identity, VPN transports and support diagnostics. Included native sources/licenses match the APK.
- Requires the new website harvest-prices endpoint for valuation. New live gameplay capture remains beta; sessions stay local and existing Loot Tracker gates are unchanged.

## 0.8.1 - 2026-10-24

- Hardened proprietary Java and WebView implementation code while preserving JNI and JavaScript bridge contracts.
- Kept private diagnostic mappings outside public artifacts and preserved safe support diagnostics.
- Passed post-obfuscation collector/profile regressions, browser scenarios and DEX/package checks.
- Replaces the unprotected 0.8.0 APK; native sources/licenses remain available. Live VPN testing limits from 0.8.0 still apply.

## 0.8.0 - 2026-10-24

- Built-in WireGuard, AmneziaWG and OpenVPN profile import and game-only tunneling.
- Encrypted profile/credential storage, connection/auth/TLS status and automatic bounded support diagnostics.
- Faster market-page capture and upload, deduplication and native TUN backpressure handling.
- Includes exact matching native sources/licenses and checksums.
- Beta: the new VPN transports still require physical Android/provider testing; no website deployment is included.

## 0.6.0 вЂ” 2026-10-19

- Added the PRO / PRO+ Loot Tracker beta with explicit recording sessions.
- Observed own silver, item drops and chest loot, including Take All merges into existing inventory stacks.
- Added grouped loot cards, sorting, recent pickup details and a link to the full website journal.
- Added an account/site/server-scoped persistent queue with retries; market capture continues when loot recording ends.
- Validated protocol replay, subscription UI, four-language narrow-screen layouts and APK distribution checks. Live Android loot gameplay is still unverified.

See [Android 0.6.0 downloads](https://github.com/MargoB2402/albion-profit-android/releases/tag/v0.6.0). Windows is distributed separately at [albion-profit-overlay](https://github.com/MargoB2402/albion-profit-overlay/releases/latest).

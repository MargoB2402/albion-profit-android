# Albion Profit Sync for Android

[Android 0.9.9 beta: learning, trade and farming observations](https://github.com/MargoB2402/albion-profit-android/releases/tag/v0.9.9)

Matched server deployment is required for challenge evaluation. Planting currently has fixture-based validation; a live island check remains pending.

## Android 0.9.8 - crafting and focus tracker

[Download and release notes](https://github.com/MargoB2402/albion-profit-android/releases/tag/v0.9.8)

Completed crafting batches, observed focus/returns and real ledger links. Partial sales, exact fees and silver per focus are separate from market-price estimates. Cloud batches and accounting links require the companion API and ledger update.

## Android 0.9.7 beta

[Download APK and release notes](https://github.com/MargoB2402/albion-profit-android/releases/tag/v0.9.7)

Take-all late membership and partial-transfer fixes, touch enchantment controls, fresh device quotes ahead of stale cache, and explicit session time ranges/duration/zones. Cloud session metadata requires the companion API update; ordinary loot uploads remain compatible with the old API. Physical-device confirmation is still needed.

## Android 0.9.6 beta

[Download APK and release notes](https://github.com/MargoB2402/albion-profit-android/releases/tag/v0.9.6)

Loot value, observed fame and hourly session rates; Android world-zone header fix. Ending a loot session keeps the window open. Market estimates/unpriced items are explicit. Device verification is still needed.

## Android 0.9.5 beta

[Download APK and release notes](https://github.com/MargoB2402/albion-profit-android/releases/tag/v0.9.5)

Website API requests now use Xray directly, bypassing the game virtual TCP adapter. Zone-transition handling and early panel shutdown are improved. Local HTTPS/TLS/race checks pass; provider stability and ping still require a device retest.


## Android 0.9.4 beta

[Download APK and release notes](https://github.com/MargoB2402/albion-profit-android/releases/tag/v0.9.4)

Happ JSON server selection, split SOCKS reply handling, world-zone display and network diagnostic categories. Provider stability still requires a device retest.


## Android 0.9.3 beta

[Download APK and release notes](https://github.com/MargoB2402/albion-profit-android/releases/tag/v0.9.3)

Android 0.9.3 beta adds an embedded VLESS/Xray transport.

- Import one VLESS connection link or Xray JSON: TCP/gRPC with TLS or Reality, HTTPUpgrade with TLS. Subscription URLs, HTTPUpgrade+Reality, unsupported transports and insecure TLS are rejected.
- Albion traffic, DNS and application API requests use one VPN service. Xray outer sockets are protected from VPN loops; local TCP proxy access requires random per-session credentials. Game UDP remains observable before encryption/after decryption.
- Profiles are stored encrypted on the device. Imported listeners, routing, logs, API/file settings and unrelated outbounds are not executed. No imported profiles or provider credentials are included in release assets.
- Existing privacy and subscription checks remain in place. External Happ alone remains tools-only; use the imported connection inside the overlay for game capture.

Setup: install this APK over the previous beta. Export ONE supported connection from Happ, not its subscription URL. Select VLESS/Xray in the overlay, import the link/JSON, then start and accept Android replacing the external VPN. Do not try to run both VPN services at once. Your provider must allow UDP. Never post private links or subscription tokens in a public issue.

Checks: local VLESS TCP/UDP roundtrips through TCP/TLS, gRPC/TLS, HTTPUpgrade/TLS, TCP/Reality and gRPC/Reality; authenticated SOCKS proxy, malformed profile/IPv6 import, Go race/WG/AWG regressions, post-R8 JVM tests, four native ABIs/16KiB alignment, matching source and hardened JNI/WebView checks. The signing identity is unchanged. No physical-phone/provider test was available: confirmation with the actual player's connection is still required.

Includes APK, complete matching native/dependency source (also exportable inside the app), license notices and SHA256SUMS.txt. Private Java/WebView implementation, credentials and obfuscation maps are excluded. Previous releases remain available for rollback.

Для проверки: установите APK поверх прежней версии, экспортируйте из Happ одно подключение VLESS и импортируйте его в пункте VLESS/Xray оверлея. Нужна ссылка vless:// или JSON самого подключения, а не адрес подписки. Запустите захват и подтвердите замену внешнего VPN. Проверьте рынок и отправку цен; для сбора после запуска захвата один раз смените локацию. Проверка на сервере вашего провайдера ещё нужна.


## Android 0.9.2 beta

[Download and release notes](https://github.com/MargoB2402/albion-profit-android/releases/tag/v0.9.2)

Android 0.9.2 beta improves built-in VPN API routing and gathering identification.

- With an imported WireGuard, AmneziaWG or OpenVPN profile, Albion traffic and this app's website/API requests use the built-in tunnel. The tunnel's outer sockets are protected from routing loops; other apps keep normal networking.
- Account verification runs after the built-in tunnel starts. Price uploads wait for successful verification and respect server-enforced private mode.
- Gathering accepts signed character IDs and validated complete zone-entry responses. The free gathering tab shows when character identification or game capture is missing, with seven-language instructions and aggregate counters.

Update by installing the APK over the previous beta; the signing identity and local settings are preserved. A real provider/server profile is required. An external Happ VPN alone does not enable capture: Android tools-only mode is still separate. Existing subscription gates remain unchanged.

Checks: encrypted WG/AWG game/TCP packet roundtrips, Go race tests, four native ABIs, JNI/R8, post-obfuscation JVM regressions, protected UI and narrow-screen checks. There is no connected physical phone; provider-specific Android connectivity and the reported live gathering issue are not yet confirmed. Missing earlier harvest is not reconstructed.

APK, matching native source archive and SHA256SUMS.txt are attached. Private Java/UI sources, credentials and obfuscation mappings are not published.


## Android 0.9.1 beta - Market support diagnostics

**[Download APK 0.9.1](https://github.com/MargoB2402/albion-profit-android/releases/download/v0.9.1/AlbionProfitSync-0.9.1.apk)** — Android 8+.

Automatic support reports distinguish market requests/responses, unknown locations and rejected rows, and identify VPN capture revocation separately. Existing capture, gathering and fishing remain available. This update investigates missing prices; it does not add Happ profile support or claim a confirmed fix for every VPN issue. The website must deploy the updated diagnostic sanitizer to retain the new fields. No manual report switch is needed.

## Android 0.9.0 beta - Gathering and fishing

**[Download APK 0.9.0](https://github.com/MargoB2402/albion-profit-android/releases/download/v0.9.0/AlbionProfitSync-0.9.0.apk)** - Android 8+ - Phones and tablets - No separate PCAPdroid installation.

The free **Gathering & fishing** tab adds local recording sessions, grouped resources/fish, and seven-city sale estimates. Choose instant sale or sell orders, configure fees/freshness, and expand each item for time, location and quantity. The website must have the new harvest-prices endpoint for valuation. Estimates do not guarantee that all items will sell. New live capture still needs physical-device gameplay testing; existing Loot Tracker gates are unchanged.

Public direct-install beta for [Albion Profit Hub](https://albionprofithub.com/overlay#android) and [Albion Profit](https://promptly.sbs/overlay#android). Windows is distributed separately at [albion-profit-overlay](https://github.com/MargoB2402/albion-profit-overlay/releases/latest).

## Install and connect

1. Install the APK over the previous Android beta. The signing identity is unchanged. Allow installation from your browser/Files app if Android asks.
2. Enter your website, account and overlay key from the website profile. Select the actual game server and private/shared prices. Do not use your website password as the overlay key.
3. Choose a connection mode:
   - **Direct capture:** local forwarding without a remote VPN server. If another VPN is active, it is preserved and only floating tools open; price capture is unavailable in that mode.
   - **WireGuard / AmneziaWG:** import your provider's .conf. Supported AmneziaWG obfuscation parameters are detected and retained.
   - **OpenVPN:** import a self-contained client .ovpn with embedded CA/certificates/keys. Enter VPN login/password and private-key password only if required by your provider.
4. Tap Connect and accept Android VPN consent. Built-in VPN mode replaces another VPN after confirmation. Albion and this app's website/API requests use this tunnel; other apps retain normal networking. Reconnect Albion after starting capture.
5. Browse a city market. Full-page price collection does not require opening every item. Allow display over other apps for the floating APH panel.

A working VPN server/provider profile is required. APH does not provide a VPN gateway. Closed app subscriptions and Amnezia vpn:// links cannot be imported directly. OpenVPN external-file profiles, scripts, proxies, PKCS#11 and interactive MFA are unsupported. TLS server certificate verification is enforced. Profiles, keys and credentials are encrypted with Android Keystore and can be deleted in settings.

## Client hardening

Version 0.8.1 shrinks and renames proprietary Java implementation code and obfuscates the packaged WebView JavaScript. Native bridge contracts are preserved. Source maps, original application UI sources and private diagnostic mappings are not distributed. Required open-source native sources and licenses remain included. Obfuscation increases reverse-engineering effort; it is not an absolute copying barrier.

## Features

- Observed market price collection and account synchronization with private price settings preserved.
- Floating price comparison, transport, crafting, enchanting, loot split, alerts, favorites and outbid tools; website account/subscription rules apply.
- Existing Loot Tracker and Island Tracker beta modules. This update does not add fishing/gathering capture or establish live loot correctness.
- Faster market uploads with bounded queues and deduplication of recently acknowledged unchanged prices.
- Automatic important technical diagnostics, including connection/authentication/TLS status. Reports exclude VPN profiles, keys, endpoints, chat and raw packets. No manual send action is required.

Server operators must deploy the corresponding mobile intake and diagnostics backend changes to accept new engine codes and faster uploads. A GitHub release does not deploy the websites.

## Validation and beta limits

Local WireGuard/AmneziaWG authenticated encrypted round trips passed with Go race detection. The actual OpenVPN packet relay passed bidirectional payload/filter/stop tests. Profile validation, market decoder regressions and APK/signature checks passed. The universal APK includes four ABIs with 16 KiB ELF alignment and excludes debug instrumentation.

**The new VPN transports have not yet been verified on a physical Android device or real provider network.** OpenVPN encrypted connectivity, Albion zone changes, long sessions and Wi-Fi/mobile transitions still need live testing. Earlier tablet market tests apply to previous versions, not these new transports. This is not a Google Play release; updates are installed from GitHub Releases.

## Feedback

[Report a problem](https://github.com/MargoB2402/albion-profit-android/issues/new?template=android-bug.yml), [suggest an improvement](https://github.com/MargoB2402/albion-profit-android/issues/new?template=android-idea.yml), or [Discord](https://discord.gg/yrP8RZJCwQ).

Include device/Android/app versions, selected transport, server/city and reproduction steps. Do not post VPN profiles, passwords, overlay keys or raw network captures. Support diagnostics are collected automatically for authorized accounts when the updated website endpoint is available.

## Checksums, source and licenses

Each release includes SHA256SUMS.txt and the exact native-source archive extracted from its APK. The app's Licenses screen also exports it without signing in. It includes matching sources, pinned revisions, build instructions and original notices for WireGuard/AmneziaWG (MIT), OpenVPN Core and our adapter (MPL-2.0 option), mbedTLS and dependencies, zdtun/JNI (LGPL-3.0-or-later).

This repository is for app distribution and public documentation. It does not publish or grant an open-source license to the website or all commercial app components. Individual bundled licenses apply to their covered components. Website access remains subject to account/subscription rules.

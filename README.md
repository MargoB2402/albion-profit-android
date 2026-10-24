# Albion Profit Sync for Android

## Android 0.8.1 beta - Hardened client and VPN transports

**[Download APK 0.8.1](https://github.com/MargoB2402/albion-profit-android/releases/download/v0.8.1/AlbionProfitSync-0.8.1.apk)** - Android 8+ - Phones and tablets - No separate PCAPdroid installation.

Public direct-install beta for [Albion Profit Hub](https://albionprofithub.com/overlay#android) and [Albion Profit](https://promptly.sbs/overlay#android). Windows is distributed separately at [albion-profit-overlay](https://github.com/MargoB2402/albion-profit-overlay/releases/latest).

## Install and connect

1. Install the APK over the previous Android beta. The signing identity is unchanged. Allow installation from your browser/Files app if Android asks.
2. Enter your website, account and overlay key from the website profile. Select the actual game server and private/shared prices. Do not use your website password as the overlay key.
3. Choose a connection mode:
   - **Direct capture:** local forwarding without a remote VPN server. If another VPN is active, it is preserved and only floating tools open; price capture is unavailable in that mode.
   - **WireGuard / AmneziaWG:** import your provider's .conf. Supported AmneziaWG obfuscation parameters are detected and retained.
   - **OpenVPN:** import a self-contained client .ovpn with embedded CA/certificates/keys. Enter VPN login/password and private-key password only if required by your provider.
4. Tap Connect and accept Android VPN consent. Built-in VPN mode replaces another VPN after confirmation. Only Albion uses this tunnel; other apps retain normal networking. Reconnect Albion after starting capture.
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

# Albion Profit Sync for Android

## Loot Tracker beta — 0.6.0

Start capture, show the floating overlay, open **Loot**, then tap **Start loot session**. Automatic loot recording and account history require **PRO or PRO+**. Each stop/start creates a separate session. Market capture continues while loot recording is stopped; already queued loot continues uploading.

The collector observes own silver after taxes, item drops and chest pickups, including merges into existing stacks. Unlinked bank/craft inventory updates and requests without confirmation are not counted. Loot is sent privately to your selected account, site and game server. Queue storage survives service restarts and retries failed uploads.

The floating Loot tab shows the 24 most recently seen loot types, sorts by quantity/value/latest/name and expands up to 20 recent pickups per card. Use the website `/loot-logger` page for full account history, session filters and splitting. Website/server 1.9.0 updates are needed to retain session metadata. CSV file import and splitting on the website remain free.

Synthetic protocol, six-stack chest replay, subscription UI, narrow-screen and APK package checks passed. **Android loot capture has not yet been verified in live gameplay.** Encrypted or unobserved packets cannot be reconstructed. This is a separate Android beta; it does not replace the Windows updater.

Public Android beta downloads and device feedback for [Albion Profit Hub](https://albionprofithub.com/overlay#android) and [Albion Profit](https://promptly.sbs/overlay#android).

**[Download APK 0.6.0](https://github.com/MargoB2402/albion-profit-android/releases/download/v0.6.0/AlbionProfitSync-0.6.0.apk)** · Android 8.0+ · Phones and tablets · No separate PCAPdroid installation

## What it does

- Collects prices from Albion markets you open and synchronizes them with your website account.
- Preserves private price settings. The server enforces your subscription for paid analytics and actions.
- Offers floating city prices, transport, crafting, enchanting, loot split, alerts, favorites and outbid listings.
- Uses vertical navigation and narrow-screen layouts, with complete item search and tier/enchantment filters.
- Optional private Island Tracker beta: observed crops and animals, estimated timers and confirmed farming actions. View state and recent history in the floating Islands tab (PRO+), with full history on the website.

## Island Tracker beta — 0.5.1

Enable **Island tracking (beta)** in the app settings before starting capture, then enter an island and approach crops or animals. Collection and server storage require PRO+. Collection is off by default and remains private, including when market prices are shared. Queued records survive restarts and retry after connectivity failures; queued/sent counters appear in the app and Islands panel.

Timers reflect the last observed state. Planting, care actions and automatic Focus attribution are not recorded yet; unseen actions while you are away are not tracked. This new tracker has passed synthetic protocol and UI checks, but has **not yet been verified on a real island or Android device**. The earlier market capture test does not validate island tracking. Feedback from island owners is welcome.

## Install

1. Download the APK on your Android device and open it. If asked, allow installation from that browser or Files app.
2. Choose your website, account and overlay key from your website profile. Use the overlay key, not your password. Choose the actual Albion region and private/shared prices.
3. Tap Connect. Approve Android's local VPN consent once. For the floating panel, separately allow display over other apps.
4. Enter Albion, move into a city, and browse a market. If capture started while already in town, change zones once first. Tap APH to open the panel.

Capture/forwarding is local to the device and limited to Albion. No remote VPN gateway, root, TLS certificate or game modification. Android allows one active VPN per profile. iOS is not supported.

This is a public direct-install beta before a future Google Play release. It was live-tested with market prices on an Android 16 tablet; other hardware and long sessions need community feedback. Google Play review/testing has not been represented as completed. App updates currently mean downloading and installing a newer APK from Releases.

## Feedback

[Report a problem](https://github.com/MargoB2402/albion-profit-android/issues/new?template=android-bug.yml), [suggest an improvement](https://github.com/MargoB2402/albion-profit-android/issues/new?template=android-idea.yml), or [talk on Discord](https://discord.gg/yrP8RZJCwQ).

Include device model, Android/app versions, server/city and steps to reproduce. For performance reports, mention whether the floating panel was open. Do not post passwords, overlay keys or raw network captures.

## Checksums and native source

Each release includes SHA256SUMS.txt and the matching native source ZIP. The APK also exposes licenses and source export without signing in. zdtun and the JNI adapter are LGPL-3.0-or-later; copyright, complete license text, pinned source revision and rebuilding/replacement instructions are included in the native archive. The shared library is dynamically linked.

This repository distributes the app; it does not grant an open-source license to the website or all app components. See the individual bundled licenses for their terms. Website access remains subject to your account and subscription.

## Русский

Скачайте APK по ссылке выше и установите через браузер или «Файлы». Отдельный PCAPdroid не нужен. Подключите аккаунт ключом оверлея из профиля сайта, выберите сервер игры и разрешите локальный VPN; для панели APH — показ поверх приложений. Войдите в город и откройте рынок. Платные функции доступны по подписке сайта.

Для отзыва укажите модель устройства, Android, версию приложения и шаги до ошибки. Ключи и пароли не публикуйте. Это открытая бета; публикация в Google Play ещё впереди.

Android 0.9.3 beta adds an embedded VLESS/Xray transport.

- Import one VLESS connection link or Xray JSON: TCP/gRPC with TLS or Reality, HTTPUpgrade with TLS. Subscription URLs, HTTPUpgrade+Reality, unsupported transports and insecure TLS are rejected.
- Albion traffic, DNS and application API requests use one VPN service. Xray outer sockets are protected from VPN loops; local TCP proxy access requires random per-session credentials. Game UDP remains observable before encryption/after decryption.
- Profiles are stored encrypted on the device. Imported listeners, routing, logs, API/file settings and unrelated outbounds are not executed. No imported profiles or provider credentials are included in release assets.
- Existing privacy and subscription checks remain in place. External Happ alone remains tools-only; use the imported connection inside the overlay for game capture.

Setup: install this APK over the previous beta. Export ONE supported connection from Happ, not its subscription URL. Select VLESS/Xray in the overlay, import the link/JSON, then start and accept Android replacing the external VPN. Do not try to run both VPN services at once. Your provider must allow UDP. Never post private links or subscription tokens in a public issue.

Checks: local VLESS TCP/UDP roundtrips through TCP/TLS, gRPC/TLS, HTTPUpgrade/TLS, TCP/Reality and gRPC/Reality; authenticated SOCKS proxy, malformed profile/IPv6 import, Go race/WG/AWG regressions, post-R8 JVM tests, four native ABIs/16KiB alignment, matching source and hardened JNI/WebView checks. The signing identity is unchanged. No physical-phone/provider test was available: confirmation with the actual player's connection is still required.

Includes APK, complete matching native/dependency source (also exportable inside the app), license notices and SHA256SUMS.txt. Private Java/WebView implementation, credentials and obfuscation maps are excluded. Previous releases remain available for rollback.

Для проверки: установите APK поверх прежней версии, экспортируйте из Happ одно подключение VLESS и импортируйте его в пункте VLESS/Xray оверлея. Нужна ссылка vless:// или JSON самого подключения, а не адрес подписки. Запустите захват и подтвердите замену внешнего VPN. Проверьте рынок и отправку цен; для сбора после запуска захвата один раз смените локацию. Проверка на сервере вашего провайдера ещё нужна.

Android 0.9.5 beta — direct website API transport inside Xray

- In VLESS/Xray mode, authenticated website requests now dial through the active Xray core directly. They bypass Android TUN, zdtun synthetic TCP and the local SOCKS listener. Game traffic continues through capture; API traffic is no longer competing inside that adapter. There is no direct-network fallback if the Xray request fails. Other transport modes retain their existing API path.
- HTTPS certificate and hostname verification remain enabled. The native request bridge accepts only HTTPS API paths on promptly.sbs and albionprofithub.com, rejects redirects and other destinations, bounds input/output and concurrent connections, preserves Retry-After and cancels pending requests when the tunnel stops. Tokens and provider configuration are not logged or included in diagnostic output.
- Location display accepts numeric zone IDs, complete Join-shaped replies under alternate operation codes, and valid successful game-server lookup replies. Empty/incomplete Join replies no longer erase the visible zone. A lookup destination does not supply an auction location for price uploads. The existing catalog includes Yew Wood and Birchcopse.
- The floating panel is removed before waiting for capture/network cleanup when stopping the service.

Checks: actual HTTPS POSTs through local VLESS TCP/TLS, gRPC/TLS, HTTPUpgrade/TLS, TCP/Reality and gRPC/Reality fixtures; invalid API certificates rejected, redirects blocked, 429/Retry-After preserved, response bounds, timeout classification and pending-request cancellation on shutdown. Full Go race suite, post-R8 JVM regressions and four-ABI/package/JNI hardening checks pass.

Install over 0.9.4; the signer and encrypted profile storage are unchanged. Reconnect capture and change zones once, then browse the market and check whether sent counts continue growing. Report failures with a fresh support export. The sent counter is per capture session; its reset does not mean previously accepted prices were deleted. Stability and ping on the actual provider/device still require confirmation.

Русский:

В режиме VLESS/Xray запросы к сайту теперь идут напрямую внутри активного Xray, без виртуального TCP-адаптера игры. Проверка HTTPS-сертификатов сохранена; обхода VPN при ошибке нет. Расширено определение зон при переходах. При остановке окно убирается до ожидания сетевых потоков.

Установите поверх 0.9.4, переподключите захват, один раз смените зону и проверьте рынок. Нужна повторная проверка роста числа отправленных цен и пинга на телефоне. Обнуление счётчика после нового запуска само по себе не означает удаления принятых сайтом цен.

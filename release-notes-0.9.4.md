Android 0.9.4 beta

- Happ JSON with multiple VLESS outbounds now opens a server picker. Only the selected connection is imported; supplied routing, listeners and logging are not executed. Existing encrypted profile storage and TLS verification remain unchanged.
- SOCKS5 reply headers are buffered across partial TCP reads. The previous parser could close a valid connection when a HELLO, authentication or CONNECT header arrived in pieces. Tests reproduce the old failure and cover every CONNECT split and byte-by-byte replies. This fixes a confirmed parser defect; the intermittent upload failures reported on a real provider still require a device retest.
- The overlay and main status show ordinary world-zone names from the existing 1,021-zone catalog. Display locations remain separate from accepted market cities. Unknown zones show their ID.
- VLESS status no longer continues to show successful API access while market upload state is offline. Network diagnostics include a numeric category (1 DNS, 2 connection, 3 timeout, 4 TLS, 5 socket/EOF, 6 other IO), without exception text or server addresses. Retaining this new category remotely requires the updated website overlay-diagnostics.js.

Install over the previous beta. In VLESS/Xray mode paste the Happ JSON, select one of the offered servers, then connect and accept Android replacing the external VPN. On this updated build, re-enter a zone and browse the market. Please report whether sent counts continue increasing. Actual provider stability is not yet confirmed.

Checks: all post-R8 JVM regressions; both VLESS outbounds from the privately supplied profile validate independently; four native ABIs with 16 KiB alignment; matching complete native source; unchanged APK signing identity; hardened DEX/JNI/WebView checks. Private provider configuration is not included in assets or sources.

Русский:

JSON Happ с несколькими VLESS-серверами теперь открывает выбор сервера. Исправлена обработка разделённых TCP-чтений ответов SOCKS. В панели и главном окне отображаются названия зон вне городов. Исправлен устаревающий статус доступа к API; добавлены числовые категории сетевых ошибок без адресов и ключей.

Установите APK поверх предыдущей версии. В режиме VLESS/Xray вставьте JSON, выберите сервер и нажмите «Подключить и начать сбор». Подтвердите замену внешнего VPN. Затем смените зону и проверьте рынок и рост числа отправленных цен. Стабильность на реальном сервере провайдера ещё нужно подтвердить.

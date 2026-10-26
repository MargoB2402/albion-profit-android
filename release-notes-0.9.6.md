# Android 0.9.6 beta — 26 October 2026

- Loot sessions show personal silver, collected item value, their combined total, observed fame and hourly rates. Missing item estimates can use exact-quality public sell quotes no older than 24 hours; the lowest city quote is labelled as an estimate, not sale proceeds. Unpriced items remain visible and the total is marked partial.
- Fame records only awards to the known local character, including reported premium, satchel and quick-learn components. Cumulative fame and duplicated destiny-board credits are not added. This is observed fame, not a guaranteed PvE-only category.
- Latest session totals survive upload acknowledgements and are saved locally. Only a new session resets them. Ending recording freezes the session clock and keeps the floating window open. Stopping capture still closes its window and VPN.
- Fixed the Android header reading the market-city field instead of the resolved world-zone name. Market requests continue to use the validated city.
- A missing item-catalog result now shows an empty-price state instead of an internet error. The companion server update looks up exact indexed game IDs, including dungeon maps missing localized names. This server fix must be deployed separately.

Install over the previous beta. Signer unchanged. Start capture, change zone once, start a loot session, collect silver/items and earn fame; check totals, then end the session and verify the window remains usable. Provider stability/ping and the zone header still require a real-device check.

Checks: post-R8 JVM regressions including fame bonuses/dedup and map-not-found handling; four native ABIs and 16 KiB alignment; hardened JNI/WebView package checks; shared valuation/session persistence tests; Android UI at 280/320/448 px with subscription gates, session transitions and seven languages. No physical phone was available.

Native source ZIP is byte-identical to the corresponding source archive inside this APK. Private Java/WebView sources, user profiles, credentials and obfuscation maps are excluded.

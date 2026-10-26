# Android 0.9.7 beta — 26 October 2026

- Fixed two reproducible take-all pickup defects: late item-to-chest membership must keep the remaining batch pending; arrival of one object must not confirm the entire transfer. Stack merges, failed moves and duplicate observations remain guarded.
- Initial and target enchantment levels now use accessible touch buttons instead of a native select popup inside the floating WebView. Tested at 280 px in seven languages. Base item tier is unchanged.
- Recent exact item/city/quality/side quotes observed on the device take priority over older API/cache values when drawing the price table. Repainting no longer waits for an upload acknowledgement or the 30-second API cache interval. Quotes expire after two minutes, cannot overwrite a newer per-side API timestamp and do not bypass locks or quality restrictions. A visible note distinguishes local observation from server upload confirmation.
- New loot sessions display start, finish, duration and pickup zones with a timezone. Their metadata is queued durably and can sync to subscriber cloud history for 30 days. Ending a session keeps the overlay open. Older sessions without explicit boundaries cannot be reconstructed reliably.

Cloud session history requires the companion server update. Until deployed, loot uploads continue and session metadata waits on the device with a separate status message. No provider profiles, user credentials or raw captures are included.

Checks: both take-all regressions fail on the 1.10.6 source and pass after the fixes; Go client/Photon suites; post-R8 JVM tests including stack transfer, late membership, partial arrival, stale/newer price selection and access gates; real PostgreSQL-compatible session schema/upsert/expiry tests; account isolation and old-server compatibility; Android touch/session browser checks in seven languages; four ABIs, 16 KiB alignment and hardened APK checks. No physical phone was available. Repeat a real chest take-all, touch selection and fresh-price scan on the user's device.

Install over 0.9.6; signer unchanged. Matching native source archive is also embedded in the APK. Private Java/WebView source and obfuscation maps are not published.

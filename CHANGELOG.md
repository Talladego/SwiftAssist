# Changelog

## 2.4.6 (2026-10-11)

- SwiftAssist / SwiftSmartAssist macros use `/assist Name` (bare name).
- Strip name grammar suffixes (`^F` / `^M`) so assist matches portrait menu.
- Persist last assist target across reload via saved variables.
- `SwiftAssist.Assist()` no longer tries `SendChatText("/assist …")` from script
  (client ignores that path); prints guidance to use the hotbar macro.
- Remove temporary TestHook helpers.

## 2.4.4

- Upstream stable (Aktheon) — text fixes. See Idrinth listing.

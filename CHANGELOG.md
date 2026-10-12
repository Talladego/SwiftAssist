# Changelog

## 2.4.8 (2026-10-12)

- Restore the saved `/assist Name` macro only when its text differs from the current slot.
  Avoids a lingering or double-consumed announce-suppress flag when `Initialize` and
  `MACROS_LOADED` both run, or when `SetMacroData` raises no `MACRO_UPDATED`.

## 2.4.7 (2026-10-11)

- Suppress "Assisting X" chat announce when restoring the saved assist macro on login/reload.
- Guard `ParseEntry` against malformed chat lines (missing `[` / `]`).
- Nil-guard `Addon.Settings` when updating `AssistTarget` from `Assist()`.

## 2.4.6 (2026-10-11)

- SwiftAssist / SwiftSmartAssist macros use `/assist Name` (bare name).
- Strip name grammar suffixes (`^F` / `^M`) so assist matches portrait menu.
- Persist last assist target across reload via saved variables.
- `SwiftAssist.Assist()` no longer tries `SendChatText("/assist …")` from script
  (client ignores that path); prints guidance to use the hotbar macro.
- Remove temporary TestHook helpers.

## 2.4.4

- Upstream stable (Aktheon) — text fixes. See Idrinth listing.

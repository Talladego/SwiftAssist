# SwiftAssist 2.4.6 (RoR assist fix)

Maintained fork of **Swift Assist** (Yakar / Wothor / Aktheon) for
[Return of Reckoning](https://www.returnofreckoning.com/).

## Why this fork

The client ignores `/assist` when it is sent from addon Lua (including
`/script SwiftAssist.Assist()`). Portrait Assist still works because it stays
on the stock UI path.

This build makes **SwiftSetAssist** write a hotbar macro of:

```text
/assist PlayerName
```

with name grammar suffixes (`^F` / `^M`) stripped to match the portrait menu.

## Usage

1. Install into `Interface\AddOns\swift-assist\` (or `SwiftAssist\`).
2. Drag **SwiftSetAssist** and **SwiftAssist** to your hotbar.
3. Target an ally → **SwiftSetAssist**.
4. Press **SwiftAssist** to take their target.

Also install **LibSlash 3.0.1+** (assist tail-call) if you type `/assist` in chat:
https://github.com/Talladego/LibSlash

## Notes

- Old macros of the form `/script SwiftAssist.Assist()` will not assist; use the
  hotbar macro text written by SetAssist.
- Other addons that call Lua during hotbar clicks can still block `/assist`
  (older GCDsaver / CustomUI / StockPiler3 wrappers). Portrait Assist working
  while the macro fails is a strong signal of that.
- Engine issues for out-of-party / siege assist may still exist separately:
  https://bugs.returnofreckoning.com/view.php?id=17526

## Credits

Original authors: **Yakar**, **Wothor**, **Aktheon**.
Assist-macro maintenance: Talladego.

Upstream listing: https://tools.idrinth.de/addons/swiftassist/

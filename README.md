# IGY6 Gaming – CMS21 Multiplayer Mod Pack

**Version 1.2.1** · Car Mechanic Simulator 2021 · MelonLoader 0.5.7

Two extra working lifts outside your garage (**Bay C** and **Bay D**), multiplayer sync fixes for CMS21-Together, an in-game building and prop editor, and preconfigured IGY6 settings.

Created and live tested by the **IGY6 Gaming Team**.

---

## Features

- **Two extra lifts** (Bay C / Bay D), registered as real car positions. They work in multiplayer and save and reload with your garage.
- **Multiplayer fixes** for CMS21-Together, applied as runtime patches (Together itself is untouched):
  - first-time joiners get their own item range (no duplicate items)
  - mid-session joiners get the live money
  - inventory and money resync after visiting the race track, junkyard and other areas
  - car positions are restored after returning
  - guards for empty-lift moves and late packets from disconnected players
- **Tools on the new bays:** oil drainer, welder, engine crane, headlamp aligner, detailing kit and window tint kit.
- **Placement editor** to move and rotate the outside building and both lifts.
- **Prop editor** to copy game props into your building and arrange them.

---

## Requirements

Install these first, following each creator's instructions:

| Mod | Version | Link |
|---|---|---|
| MelonLoader | **0.5.7** | [Releases](https://github.com/LavaGang/MelonLoader/releases) |
| TogetherMod | **Release-0_4_16hf3** | [Fozkais/CMS21-Together](https://github.com/Fozkais/CMS21-Together) |
| FixesForTogether | latest | [Nexus Mods #286](https://www.nexusmods.com/carmechanicsimulator2021/mods/286) |
| QoLmod | latest | [Nexus Mods #105](https://www.nexusmods.com/carmechanicsimulator2021/mods/105) |

> The game must be the up-to-date **Steam** version, launched through Steam.

---

## Installation

1. Install **MelonLoader v0.5.7**. Launch the game once, reach the main menu, then close it.
2. Install **TogetherMod**, **FixesForTogether** and **QoLmod**.
3. Extract the IGY6 Mod Pack.
4. Drag all **loose files** from the pack **directly** into the game's `Mods` folder (not into a subfolder).
5. Drag the **contents** of the pack's `FixesForTogether` and `QoLmod` folders into the matching folders inside `Mods`.
6. Drag the included `MelonPreferences.cfg` into the game's `UserData` folder.
7. Choose **only one** of the 3 maps and drag its assets into `Mods`. We suggest the **Large Garage**.
8. Choose **"Replace the files in the destination"** whenever Windows asks.

Keep only **one** copy of `IGY6FourBayMod.dll` in `Mods`.

**Default game location**

```
C:\Program Files (x86)\Steam\steamapps\common\Car Mechanic Simulator 2021
```

---

## Multiplayer

1. Launch CMS21 and select **Multiplayer**.
2. Change the connection from **TCP** to **Steam**.
3. Invite your friends with your join ID and start your save.

> **Important:** all players must use the same required mods, the same IGY6 pack files and the same map.
> If you change the building placement or props, share `IGY6TwoBay_Placement.cfg` and `IGY6TwoBay_Props.cfg` from your `Mods` folder.

---

## Hotkeys

### Cars

| Keys | Action |
|---|---|
| `Ctrl + H` or `Ctrl + 7` | Waiting car → **Bay C** (outside left lift) |
| `Ctrl + K` or `Ctrl + 9` | Waiting car → **Bay D** (outside right lift) |

Shift is optional (`Ctrl + Shift + 7 / 9` also works).

### Tools

| Keys | Action |
|---|---|
| `Ctrl + Shift + C` or `Ctrl + Shift + ←` | Nearest tool → Bay C |
| `Ctrl + Shift + D` or `Ctrl + Shift + →` | Nearest tool → Bay D |
| `Ctrl + Shift + 3` | Nearest tool → nearest bay with a car |

Press the same keys again to send the tool back. Tools only move to a bay with a car on it.

### Building and props

| Keys | Action |
|---|---|
| `Ctrl + Shift + P` | **Placement editor**: move / rotate the outside building and both lifts (solo only, Bay C and D empty and lowered) |
| `Ctrl + Shift + O` | **Prop editor**: copy game props into your building and arrange them |

### Editor keys

| Action | Numpad | Keyboard |
|---|---|---|
| Move | `8` `2` `4` `6` | Arrow keys |
| Up / down | `9` `3` | `Page Up` `Page Down` |
| Rotate | `7` `1` | `,` `.` |
| Step size | `+` `-` | `=` `-` |
| Save | `Enter` | `Enter` |
| Copy aimed prop *(prop editor)* | `*` | `Insert` |
| Place / select *(prop editor)* | `5` | `Home` |
| Next prop *(prop editor)* | `0` | `End` |
| Remove prop *(prop editor)* | `.` | `Delete` |

Press the editor's hotkey again to close / cancel.

---

## Troubleshooting

### Ctrl + Shift hotkeys do nothing

On some PCs `Ctrl + Shift` switches the Windows keyboard language, so the game never receives the key.

1. Open `UserData\MelonPreferences.cfg`.
2. Find `[IGY6TwoBay]`.
3. Set:

   ```ini
   HotkeyModifier = "CtrlAlt"
   ```

Now use `Ctrl + Alt` instead of `Ctrl + Shift` for the tool and editor hotkeys. Other options: `"AltShift"` or `"None"`. The car keys (`Ctrl + H / K / 7 / 9`) always work.

### Multiplayer doesn't work at all

If `MelonLoader\Latest.log` shows `SteamApi_Init returned false`, the game isn't running through Steam. CMS21-Together needs the Steam version.

---

## Configuration files

| File | Location | Purpose |
|---|---|---|
| `IGY6TwoBay_Placement.cfg` | `Mods` | Position / rotation of the outside building and Bay C / D (written by the placement editor) |
| `IGY6TwoBay_Props.cfg` | `Mods` | Props copied into your building (written by the prop editor) |
| `IGY6TwoBay_Replica.cfg` | `Mods` | Optional copy of the original garage shell (off by default) |
| `MelonPreferences.cfg` | `UserData` | Settings under `[IGY6TwoBay]` (`HotkeyModifier`, `TripResyncMode`, ...) |

All players must use the same `.cfg` files in the `Mods` folder.

---

## Building from source

Requires the .NET SDK and a game install where MelonLoader 0.5.7 has run once (to generate `MelonLoader\Managed`). No game files are included in this repository.

```powershell
dotnet build -c Release -p:GameDir="C:\Program Files (x86)\Steam\steamapps\common\Car Mechanic Simulator 2021"
```

The DLL is written to `bin\Release\net472\`. Add `-p:DeployToGame=true` to copy it into your `Mods` folder. See `CHANGELOG.md` for the full history.

---

## Support

Open a **General Support Ticket** on our Discord: **[discord.gg/igy6](https://discord.gg/igy6)**

Please attach `MelonLoader\Latest.log` from the host and the affected player.

---

## IGY6 Gaming Team

| Name | Role |
|---|---|
| LordFarquadFr | Developer |
| OogieBoogie | Tester |
| Rusty | Tester |
| xL00MYx | Tester |
| CharredCheeto | Tester |

**Credits:** CMS21-Together by Fozkais · FixesForTogether by TogetherFixer · QoLmod by Meitzi · MelonLoader by LavaGang

## License

MIT, see [LICENSE](LICENSE). Not affiliated with Red Dot Games or PlayWay.

---

<p align="center"><b>I GOT YOUR 6! – IGY6 Gaming</b></p>

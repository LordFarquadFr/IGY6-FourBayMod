# IGY6 GAMING - CMS21 MULTIPLAYER MOD PACK

**Version 1.2.1** — Correct maps, new `IGY6FourBayMod.dll`, and new hotkey customization.

---

## 📋 REQUIREMENTS (INSTALL FIRST)

1. **MelonLoader v0.5.7**  
   https://github.com/LavaGang/MelonLoader/releases

2. **TogetherMod (Release-0_4_16hf3)**  
   https://github.com/Fozkais/CMS21-Together/releases/tag/Release-0_4_16hf3

3. **FixesForTogether**  
   https://www.nexusmods.com/carmechanicsimulator2021/mods/286

4. **QoLmod**  
   https://www.nexusmods.com/carmechanicsimulator2021/mods/105

**Important:** Follow each mod creator's installation instructions before installing the IGY6 pack.

The game must be the **up-to-date Steam version**, launched through Steam.

---

## 📦 INSTALLATION

1. Install **MelonLoader v0.5.7**. Launch the game once, reach the main menu, then close it.
2. Install **TogetherMod, FixesForTogether, and QoLmod**.
3. Extract the **IGY6 Mod Pack**.
4. Drag and drop all loose files from the IGY6 pack **DIRECTLY** into your game's `Mods` folder (not into a subfolder).
5. Drag and drop the contents of the IGY6 `FixesForTogether` and `QoLmod` folders into their matching folders inside `Mods`.
6. Drag and drop the included `MelonPreferences.cfg` into the game's `UserData` folder.
7. Drag the assets from **ONLY ONE** of the 3 maps into the `Mods` folder. **We suggest the Large Garage.**
8. Select **"Replace the files in the destination"** whenever prompted.

**These are preconfigured IGY6 settings and replacements. No manual configuration needed!**

### Default Game Location

```text
C:\Program Files (x86)\Steam\steamapps\common\Car Mechanic Simulator 2021
```

---

## 🎮 MULTIPLAYER

1. Launch **CMS21** and select **Multiplayer**.
2. Change the connection from **TCP** to **Steam**.
3. Invite your friends with your **Join ID** and start your save!

**Important:** All players must install the same required mods, the same IGY6 pack files, and the same map.

If you change the building placement or props, send your friends these files from the `Mods` folder so everyone matches:

- `IGY6TwoBay_Placement.cfg`
- `IGY6TwoBay_Props.cfg`

---

## ⌨️ HOTKEYS

### 🚗 Cars

| Hotkey | Action |
|---|---|
| **Ctrl + J** | Send the waiting customer car to Bay C (outside left lift) |
| **Ctrl + L** | Send the waiting customer car to Bay D (outside right lift) |

### 🛠️ Tools

Supported tools: **Oil Drainer, Welder, Engine Crane, Headlamp Aligner, Detailing Kit, Window Tint Kit**

| Hotkey | Action |
|---|---|
| **Ctrl + Shift + C** or **Ctrl + Shift + Left Arrow** | Nearest tool to Bay C |
| **Ctrl + Shift + D** or **Ctrl + Shift + Right Arrow** | Nearest tool to Bay D |
| **Ctrl + Shift + 3** | Nearest tool to the nearest bay that has a car |

**Note:** Press the same keys again to send the tool back. Tools only move to a bay with a car.

### 🏗️ Building and Props

| Hotkey | Action |
|---|---|
| **Ctrl + Shift + P** | Placement editor — move/rotate the outside building and both lifts |
| **Ctrl + Shift + O** | Prop editor — copy game props into your building and arrange them |

**Placement Editor Requirements:** Solo only, with Bay C and D empty and lowered.

### 🎛️ Editor Controls

| Action | Numpad | Keyboard Alternative |
|---|---|---|
| Move | Numpad 8 / 2 / 4 / 6 | Arrow Keys |
| Up / Down | Numpad 9 / 3 | Page Up / Page Down |
| Rotate | Numpad 7 / 1 | `,` / `.` |
| Step Size | Numpad + / - | `=` / `-` |
| Save | Numpad Enter | Enter |

### Prop Editor Only

| Numpad | Keyboard Alternative | Action |
|---|---|---|
| Numpad * | Insert | Copy the prop you aim at (it follows your aim) |
| Numpad 5 | Home | Place / Select |
| Numpad 0 | End | Next Prop |
| Numpad . | Delete | Remove Prop |

**Press the editor's hotkey again to close or cancel.**

---

## ⚙️ CHANGING THE HOTKEY MODIFIER

**If Ctrl + Shift hotkeys do nothing:**

On some PCs, **Ctrl + Shift** switches the Windows keyboard language, preventing the game from detecting the key combination.

1. Open `UserData\MelonPreferences.cfg`.
2. Find the `[IGY6TwoBay]` section.
3. Change the setting to:

```ini
HotkeyModifier = "CtrlAlt"
```

4. Use **Ctrl + Alt** instead of **Ctrl + Shift** for the tool and editor hotkeys.

**Other available options:**
- `"AltShift"`
- `"None"`

**Note:** The car hotkeys (**Ctrl + J / Ctrl + L**) never change.

---

## 🆘 SUPPORT

Report issues by opening a **General Support Ticket** in our Discord:

**[Join IGY6 Gaming Discord](https://discord.gg/igy6)**

Please attach the following log files from both the host and affected player:

```text
MelonLoader\Latest.log
```

---

## 🏆 IGY6 GAMING TEAM

| Member | Role |
|---|---|
| OogieBoogie | Tester |
| Rusty | Tester |
| xL00MYx | Tester |
| CharredCheeto | Tester |
| **LordFarquadFr** | **Developer** |

**Created and live tested by the IGY6 Gaming Team.**

---

### I GOT YOUR 6! - IGY6 Gaming

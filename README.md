<div align="center">

```
██████╗ ██╗███████╗ ██████╗██╗██╗   ██╗███████╗███████╗
██╔══██╗██║██╔════╝██╔════╝██║██║   ██║██╔════╝██╔════╝
██████╔╝██║█████╗  ██║     ██║██║   ██║███████╗███████╗
██╔═══╝ ██║██╔══╝  ██║     ██║██║   ██║╚════██║╚════██║
██║     ██║███████╗╚██████╗██║╚██████╔╝███████║███████║
╚═╝     ╚═╝╚══════╝ ╚═════╝╚═╝ ╚═════╝ ╚══════╝╚══════╝
```

**FiveM Script Developer · Frontend & Backend**

---

</div>

### whoami

```lua
local Pieciuss = {
    focus     = "FiveM Script Development",
    stack     = { "Lua", "JavaScript" },
    side      = { "Frontend", "Backend" },
    status    = "Building something cool...",
}
```

---

### stack

| Layer | Tech |
|---|---|
| **Game Scripting** | `Lua` · `FiveM Native API` |
| **Frontend (NUI)** | `JavaScript` · `HTML/CSS` |
| **Backend** | `JavaScript` · `oxmysql` |

---

### projects

> All scripts support **ESX** & **QBCore** via built-in auto-detection bridge.

---

<details>
<summary>🧩 <b>piecius_core</b> — Server Core & Vehicle System</summary>

Vehicle key & lock system (keybind `U`), hotwiring with 15% success chance, engine block without key, military vehicle blacklist (~80+ models auto-deleted), Fort Zancudo cleanup, emergency service suppression (cops, EMS, fire), wanted level disable, dispatch disable, NUI ID card system (`/id`) with SSN generation, admin key commands (`/givekey`, `/makekey`, `/handkey`).

🔗 [Repository](https://github.com/Pieciuss/piecius_core)
</details>

<details>
<summary>👥 <b>piecius_multicharacter</b> — Multi-Character Selection</summary>

Up to 3 character slots per player, full NUI selection screen with camera at custom coords, character deletion support, `/relog` command with 10s cooldown, default male/female appearance presets with full genetics, auto-detect license/IP identifier for LAN support.

🔗 [Repository](https://github.com/Pieciuss/piecius_multicharacter)
</details>

<details>
<summary>🚗 <b>piecius_garage</b> — Vehicle Garage & Impound</summary>

6 garage locations (Downtown, South LS, Airport, Paleto Bay, Sandy Shores, Vinewood), NUI panel showing vehicle name/plate/body health/engine health/fuel level/location, impound lot with NPC & $500 recovery fee, 3D floating hints, spawn point collision detection, full vehicle props persistence (body, engine, tank, dirt, fuel). Admin commands: `/garagegive`, `/garagedelete`, `/garagelist`, `/unimpound`, `/repair`, `/carwipe`.

🔗 [Repository](https://github.com/Pieciuss/piecius_garage)
</details>

<details>
<summary>💊 <b>piecius_crime</b> — Criminal Organizations System</summary>

Organization creation ($50k) with name & tag, tablet item ($15k) openable via NPC or `F6` keybind with prop animation, 6-tier rank system (Recruit→Leader) with granular permissions, purchasable upgrades (member slots up to 30, vault up to $5M, org garage up to 10 slots, armory levels), organization vault with deposit/withdraw, 6 buyable HQ locations ($80k–$350k) with instanced interiors (routing buckets), interior points (wardrobe, safe as ox_inventory stash, garage), org vehicle garage with personal↔org transfer.

🔗 [Repository](https://github.com/Pieciuss/piecius_crime)
</details>

<details>
<summary>📊 <b>piecius_hud</b> — Custom HUD & Minimap</summary>

Status bars (health, armor, hunger, thirst) updated every 250ms, vehicle HUD (speed KMH/MPH toggle, fuel, gear, seatbelt, engine state, EV indicator) updated every 100ms, dynamic minimap (visible only in vehicle), street/zone name display, pma-voice range indicator, built-in progress bar export (`Piecius_hud:Progressbar`), notification system export (`Piecius_hud:Notification`), `/cinematic` mode, `/ssn` display, `/hudon` `/hudoff` `/hudsettings`, native GTA HUD suppression, custom minimap stream.

🔗 [Repository](https://github.com/Pieciuss/piecius_hud)
</details>

<details>
<summary>🎨 <b>piecius_skin</b> — Character Appearance Creator</summary>

Full NUI skin editor with 9 categories (genetics, face, hair, beard, eyebrows, makeup, skin details, clothing, accessories), scripted orbit camera with mouse drag rotation & scroll zoom, face genetics with mom/dad/grandparent blending, 6 nose params, cheeks, jaw, chin, eye color, full clothing components (undershirt, torso, pants, shoes, mask, kevlar, chain, hat, glasses, watches, etc.), restricted/saveable editor modes, backpack weight system, skinchanger integration.

🔗 [Repository](https://github.com/Pieciuss/piecius_skin)
</details>

<details>
<summary>🪪 <b>piecius_identity</b> — Character Registration</summary>

NUI registration form for new characters (first name, last name, date of birth, sex, height), configurable validation (max 20 char names, height 120–220cm, max age 100, DD/MM/YYYY format), blur backdrop effect, loading screen gate, multicharacter integration (auto-detects Piecius_multicharacter or esx_multicharacter), locale-driven UI labels, auto-triggers skin editor after registration.

🔗 [Repository](https://github.com/Pieciuss/piecius_identity)
</details>

<details>
<summary>👔 <b>piecius_clothing</b> — Inventory Clothing System</summary>

15 clothing item types mapped to GTA components & props (mask, gloves, pants, bag, shoes, chain, undershirt, kevlar, torso, hat, glasses, ears, watch, bracelet, decal), ox_inventory integration — equip/unequip by using items, toggle behavior (use equipped item to unequip), previous state restoration, server-synced persistence, auto-reapply on spawn/model change/resource restart, exports (`getEquippedState`, `applyEquipVisual`, `applyUnequipVisual`), debug commands `/myoutfit` `/testclothing`.

🔗 [Repository](https://github.com/Pieciuss/piecius_clothing)
</details>

<details>
<summary>⛽ <b>piecius_fuel</b> — Realistic Fuel System</summary>

RPM-based fuel consumption (10 tiers) with vehicle class & per-model multipliers, decorator-based fuel storage, physical pump interaction with nozzle prop & rope physics (30m max length), walk to fuel cap & press `E` to attach, real-time NUI showing liters/price/fuel%, 29 gas stations + 5 supercharger locations with blips, jerry can system (buy $100, refuel at pump, use on vehicles with animation), 13 electric vehicle models with exponential kW charging curve, fuel cap bone detection with fallback chain, configurable pricing ($1.70/L gas, $0.30/kW electric), exports: `GetFuel`, `SetFuel`, `ApplyFuel`.

🔗 [Repository](https://github.com/Pieciuss/piecius_fuel)
</details>

<details>
<summary>💬 <b>piecius_rpchat</b> — RP Chat with 3D Hints</summary>

7 RP commands (`/me`, `/do`, `/try` with random outcome, `/ooc`, `/med`, `/twt` global, `/dw` dark web) + `/globaldo` with admin approval system, 3D floating message bubbles above player heads with 8s duration, distance-based scaling (up to 30m), configurable range per command, admin commands `/acceptglobaldo` `/denyglobaldo`, chat suggestions with parameter descriptions.

🔗 [Repository](https://github.com/Pieciuss/piecius_rpchat)
</details>

---

### contact

```
Discord → pieciuss
```

[![Discord](https://img.shields.io/badge/Discord-Join%20Server-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/uBa28BSFFC)

---

<div align="center">

*scripts that just work.*

</div>

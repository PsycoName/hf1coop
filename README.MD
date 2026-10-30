# HF1Coop

Co-op mod for **House Flipper 1**. Play with friends over UDP — ghost avatars, shared money, synced orders, and synced trash/dirt cleanup.

> Work in progress (v0.4.2). Positions, money, orders and cleaning are synced. Building/furniture placement is **not**.

---

## Requirements

- [BepInEx](https://github.com/BepInEx/BepInEx/releases)
- House Flipper 1 (Steam)
- Same mod version on all players

---

## Install

1. Install **BepInEx** and run the game once.
2. Drop `HF1Coop.dll` into `House Flipper\BepInEx\plugins\`.
3. Launch the game. Config is created at `BepInEx\config\local.hf1.coop.cfg`.

---

## Quick start

1. **Host:** press **F8**. Forward **UDP 27015** (or use a VPN like ZeroTier/Radmin).
2. **Client:** set `HostIP` in the config. Then press **F9**.
3. **Anyone:** press **F10** to disconnect.

Only the host needs a reachable IP.

---

## Features

- **👥 Ghost avatars** — see other players.
- **💰 Shared money** — one lobby-wide balance, delta-synced. New joiners get the current amount. Host can press **F11** to force everyone to match their balance.
- **📋 Synced orders** — if *anyone* has it; completion takes the max. Full state sent on load and to late joiners.
- **🧹 Synced cleanup** — trash, dirt, decal dirt and piles of rubbish disappear for everyone, including for players who join later.
- **🔄 Auto-update** — optional, SHA-256 verified DLL update via a manifest URL; applies immediately or on next launch if the DLL is locked.

---

## Controls (default)

| Key | Action |
|-----|--------|
| **F8** | Start hosting |
| **F9** | Join host |
| **F10** | Disconnect |
| **F11** | *(Host)* Push host money to everyone |

All keys rebindable in the config.

---

## Configuration

`BepInEx\config\local.hf1.coop.cfg`

**`[Net]`** — `HostIP`, `Port`.

**`[Keys]`** — `Host`, `Join`, `Stop`, `PushMoney`.

**`[Update]`** — `ManifestUrl`, `AutoUpdate`.

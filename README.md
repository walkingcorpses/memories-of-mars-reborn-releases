<div align="center">

# MEMORIES OF MARS: REBORN

**The survival game the servers left behind, playable again.**

[![Download](https://img.shields.io/badge/Download-MoMReborn--Setup.exe-f59a2e?style=for-the-badge&logo=windows&logoColor=white)](../../releases/latest)
&nbsp;
![Platform](https://img.shields.io/badge/Windows-10%20%7C%2011-1d2327?style=for-the-badge)
&nbsp;
![Steam](https://img.shields.io/badge/Needs-Steam%20copy%20of%20the%20game-1d2327?style=for-the-badge&logo=steam&logoColor=white)

<img src="images/menu.png" alt="The Reborn main menu" width="860">

</div>

---

Memories of Mars lost its official servers in June 2024, taking multiplayer, the menu's online features and the Steam
achievements with them. **Reborn** puts them back: everything runs on your own PC, and your friends can drop into your world.

## Features

| | |
|---|---|
| **Single player** | Press **SINGLE PLAYER** on the main menu. Your world starts with the game. |
| **Play with friends** | Friends who also have Reborn see your world in **PLAY ONLINE**, or accept a Steam "Join Game". No lobby, no codes to type. |
| **Achievements** | Unlocks are saved and written to Steam again. |
| **Built into the game** | REBORN is in the title logo and the mod version sits in the corner of the main menu. No overlay, no extra window, works in fullscreen at any resolution. |
| **Updates itself** | Checks this page when the game starts and installs new versions. |
| **Fully reversible** | Run the setup again and press **Uninstall** to put the game back exactly as it was. |

## Install

1. Install **Memories of Mars** from Steam.
2. Download **[MoMReborn-Setup.exe](../../releases/latest)** and run it. It finds your game by itself.
3. Press **Play** in Steam. That's it.

Your friends do the same, then you can play together.

> **First time hosting?** Reborn downloads the game's dedicated server from Valve (about 800 MB) in the background the first time. Only the person hosting needs it.

## How it works

Reborn starts a small local replacement for the game's dead online service, runs the publisher's own free dedicated server
on your PC, and edits a few of the game's files so the menu says what it should. Steam friends who are playing Reborn
find each other through Steam, so there is nothing to configure.

<details>
<summary><b>What exactly does the installer change?</b></summary>

- Swaps Steam's `Launch_Game.exe` for the Reborn launcher (the original is kept as `Launch_Game.original.exe`).
- Adds a patch pak next to the game's own pak (`pakchunk0-WindowsNoEditor_reborn_P.pak`) with the changed menu files, built on your PC from your own copy of the game.
- Patches 2 bytes of `MemoriesOfMars.exe` so the game accepts that unsigned pak (the original is kept as `MemoriesOfMars.exe.reborn-original`).
- Adds one line to the game's user `Engine.ini` so it talks to the local service.

Uninstalling reverses every one of these. The game's own pak is never modified. No game files are included in this download.
</details>

## Troubleshooting

<details>
<summary><b>My friends can't join my world</b></summary>

Your router has to let them in. Reborn asks it to open the ports automatically (UPnP). If your router doesn't allow that,
forward **UDP 7777** and **UDP 15000** to your PC in the router settings.
</details>

<details>
<summary><b>The game won't start after a Steam update</b></summary>

Start it again: Reborn repairs its changes on launch. If it still fails, run **MoMReborn-Setup.exe** once more.
</details>

<details>
<summary><b>Where are the logs?</b></summary>

`%LOCALAPPDATA%\MemoriesOfMarsReborn`
</details>

## What's new

**1.0.0** — First release: single player, friends' worlds, achievements, REBORN built into the menu, auto-update.

---

<sub>Reborn is an unofficial fan project and is not affiliated with Limbic Entertainment or 505 Games. Memories of Mars is their game; you need to own it on Steam.</sub>

# Path of the Unbound（无缚之路）

> **A single-player survival escape thriller built with Unity 6.**
> You are a fugitive. The Inquisition is hunting you. The forest does not care which of you catches you first.

[English](README_EN.md) | [简体中文](README.md)

---

## 🎮 About the Game

*Path of the Unbound* is a single-player, narrative-driven survival game. You wake in a hostile forest as a runaway — hunted by the Inquisition's hounds, pursuers, and an elite squad that closes in the longer you linger. Every step drains your body and your mind. You must decide: which wound to treat, which voice to ignore, how long you can keep running.

Every journey is different. Your survival depends on the cards you draw, the choices you make, and how far you let your body and sanity decay before they give out.

## ✨ Key Features

- **Four vital stats to juggle** — Health, Stamina (STA), Sanity (SAN), and Satiety (SAT). Let any one of them collapse and the forest wins.
- **Pursuit system** — an ever-tightening net. Hounds bark in the distance, torches move through the trees, and if your Pursuit Level maxes out, an elite squad surrounds you.
- **Card-driven event system** — travel events are drawn from card pools (a common pool plus distinct Stage 1 and Stage 2 pools), each with branching consequences, costs, and outcomes.
- **Buffs & Debuffs** — bleeding, poison, hunger, wounds that refuse to heal, and whispers that erode your sanity. Manage them, or die carrying them.
- **Two stages, one forest** — from the dark woods to the Misty Lake, the environment (and the danger) evolves as you progress.
- **Multiple endings** — how you die (or escape) depends on how you played.
- **Rich atmospheric presentation** — dynamic status warnings, card hover effects, crossfading BGM, and a heartbeat that quickens when the hounds are near.

## 🕹️ Core Systems

| System | Description |
| --- | --- |
| **Health** | Your physical condition. Wounds, poison, and starvation chip away at it. |
| **Stamina (STA)** | The fuel for action. Many cards cost stamina — insufficient STA blocks the choice. |
| **Sanity (SAN)** | Your mental state. Fear, isolation, and whispers erode it. At zero, you break. |
| **Satiety (SAT)** | Hunger management. Starving accelerates every other decline. |
| **Pursuit Level** | How close the Inquisition is. Grows over time; some events let you evade it. |
| **Card Events** | Drawn from Common / Stage 1 / Stage 2 pools (CSV-driven). Each card changes your stats, statuses, or the pursuit. |
| **Status Effects** | Persistent buffs/debuffs (e.g. bleeding, toxin, starvation, breakdown) tracked in the status panel. |

### Status & Warnings

A status panel tracks every active buff and debuff in real time. When a stat approaches a dangerous threshold, the game raises red warnings: `Low`, `High Danger`, `Starving`, `Dying`, `Breakdown`.

Status changes from events are presented with explicit action markers, for example:

- `Bless: Gain [……]` — a buff is applied
- `Warn: Add [……]` — a debuff is added
- `Cure: Rmv [……]` — a negative status is removed

## 🗺️ Stages & Endings

- **Stage 1** — the deep forest. Learn to survive while the hounds find your scent.
- **Stage 2** — the Misty Lake region. The terrain opens up, but so does the hunt.

The end is rarely clean: lose your way and the forest takes you; get caught and the Inquisition claims you; lose your mind and you end it yourself.

## 🖥️ Controls

| Input | Action |
| --- | --- |
| Mouse wheel | Zoom camera |
| Shift + Right Mouse Button | Control camera |
| Click | Select / play cards |

## 🛠️ Tech Stack

| Category | Technology |
| --- | --- |
| Engine | Unity 6 (6000.3.6f1) |
| Render Pipeline | Universal Render Pipeline (URP) |
| Language | C# (custom assemblies: GameManager, CardManager, CardEvent, PlayerStatus, AudioManager, HintSystem, MainMenuUI, etc.) |
| UI | UGUI + TextMeshPro (rich-text event narration) |
| Input | Unity Input System |
| Graphics API | DirectX 12 |
| Data | CSV-driven card pools (`CommonCards.csv`, `Stage1Cards.csv`, `Stage2Cards.csv`) |

## 💻 System Requirements

- **OS:** Windows 10/11 (64-bit)
- **Graphics:** DirectX 12 capable GPU
- **Storage:** ~160 MB free space

## 🚀 Download & Run

1. Download the repository ZIP and extract it (or simply `git clone`).
2. Run **`Path_of_the_Unbound.exe`**.
3. No installation required.

## 📁 Project Structure

```
Path_of_the_Unbound/
├── Path_of_the_Unbound.exe          # Main executable
├── UnityPlayer.dll                  # Unity runtime
├── UnityCrashHandler64.exe          # Crash handler
├── D3D12/                           # DirectX 12 core
├── MonoBleedingEdge/                # Mono runtime
└── Path_of_the_Unbound_Data/        # Game data, assemblies & assets
    ├── Managed/                     # .NET assemblies (incl. Assembly-CSharp.dll)
    ├── Resources/                   # Built-in Unity resources
    ├── level0                       # Main scene data
    └── *.assets                     # Serialized assets (cards, UI, audio, etc.)
```

## 🔧 Development Notes

- This repository contains the **compiled Windows build** of the game (not the Unity source project); custom game logic is compiled into `Assembly-CSharp.dll`.
- Card pools are configured via CSV (`CommonCards.csv` / `Stage1Cards.csv` / `Stage2Cards.csv`). To adjust event content, edit the CSVs in the Unity project and rebuild.
- The in-game narrative text is currently in English; multi-language support is planned for future releases.

## ❓ FAQ

**Q: Why does the repository only contain build files, not source code?**
A: This repository currently hosts the playable Windows build only; the Unity source project is not included.

**Q: Can the cards be customized?**
A: Yes. Event cards are driven by CSV data — edit the card-pool CSVs in the Unity project and rebuild.

---

*Path of the Unbound — walk the unbound path.*

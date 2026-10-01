# Path of the Unbound

**A survival escape thriller built with Unity.** You are a fugitive. The Inquisition is hunting you. The forest does not care which of you catches you first.

> 中文版说明见文末 → [中文说明](#中文说明)

---

## 🎮 About the Game

*Path of the Unbound* is a single-player, narrative-driven survival game. You wake in a hostile forest as a runaway — hunted by the Inquisition's hounds, pursuers, and an elite squad that closes in the longer you linger. Every step drains your body and your mind. You must decide: which wound to treat, which voice to ignore, how long you can keep running.

Every journey is different. Your survival depends on the cards you draw, the choices you make, and how far you let your body and sanity decay before they give out.

## ✨ Key Features

- **Four vital stats to juggle** — Health, Stamina (STA), Sanity (SAN), and Satiety (SAT). Let any one of them collapse and the forest wins.
- **Pursuit system** — an ever-tightening net. Hounds bark in the distance, torches move through the trees, and if your Pursuit Level maxes out, an elite squad surrounds you.
- **Card-driven event system** — travel events are drawn from card pools (common cards plus distinct Stage 1 and Stage 2 pools), each with branching consequences, costs, and outcomes.
- **Buffs & Debuffs** — bleeding, poison, hunger, wounds that refuse to heal, and whispers that erode your sanity. Manage them or die carrying them.
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
| **Card Events** | Draw from Common / Stage 1 / Stage 2 pools (CSV-driven). Each card changes your stats, statuses, or the pursuit. |
| **Status Effects** | Persistent buffs/debuffs (e.g. bleeding, toxin, starvation, breakdown) tracked in the status panel. |

## 🗺️ Stages & Endings

- **Stage 1** — the deep forest. Learn to survive while the hounds find your scent.
- **Stage 2** — the Misty Lake region. The terrain opens up, but so does the hunt.

The end is rarely clean: lose your way and the forest takes you; get caught and the Inquisition claims you; lose your mind and you end it yourself.

## 🛠️ Tech Stack

- **Engine:** Unity 6 (6000.3.6f1)
- **Pipeline:** Universal Render Pipeline (URP)
- **Language:** C# (custom assemblies: GameManager, CardManager, CardEvent, PlayerStatus, AudioManager, HintSystem, MainMenuUI, etc.)
- **UI:** UGUI + TextMeshPro (rich-text event narration)
- **Input:** Unity Input System
- **Graphics API:** DirectX 12
- **Data:** CSV-driven card pools (`CommonCards.csv`, `Stage1Cards.csv`, `Stage2Cards.csv`)

## 💻 System Requirements

- **OS:** Windows 10/11 (64-bit)
- **Graphics:** DirectX 12 capable GPU
- **Storage:** ~160 MB free space

## 🚀 How to Run

1. Download the repository and extract the ZIP (or clone it).
2. Run **`Path_of_the_Unbound.exe`**.
3. No installation required.

### Controls

| Input | Action |
| --- | --- |
| Mouse wheel | Zoom camera |
| Shift + Right Mouse Button | Control camera |
| Click | Select / play cards |

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
    └── *.assets                     # Serialized assets (cards, UI, audio)
```

## 📝 Notes

- This repository contains the **compiled Windows build** of the game (not the Unity source project).
- The in-game narrative text is in English.

---

## 中文说明

# 无缚之路（Path of the Unbound）

一款基于 **Unity 6** 开发的单人生存逃亡叙事游戏。你是审判所追捕的逃犯，必须在黑暗的森林中活下去——猎犬在远处低吠，火把在树丛间移动，追捕的网越收越紧。

### 核心玩法

- **四项生存属性**：生命（Health）、体力（STA）、理智（SAN）、饱食（SAT），任何一项崩溃都会导致失败。
- **追捕系统**：追捕等级随时间上升，部分事件可以摆脱追捕；追捕拉满时精锐小队将包围你。
- **卡牌事件系统**：旅行事件从卡池抽取（通用卡 + 第一幕/第二幕独立卡池，由 CSV 配置），每张卡都带来不同的代价与后果。
- **增益与减益**：流血、中毒、饥饿、无法愈合的伤口、侵蚀理智的低语……你需要管理它们，或带着它们死去。
- **两个阶段**：从幽暗森林到雾湖，随着推进环境与危险都会升级。
- **多种结局**：迷失森林化为尘土、被审判所捕获、或理智崩坏自我了断——结局取决于你的选择。

### 操作

| 输入 | 动作 |
| --- | --- |
| 鼠标滚轮 | 缩放镜头 |
| Shift + 鼠标右键 | 控制镜头 |
| 单击 | 选择 / 打出卡牌 |

### 运行方式

下载仓库 ZIP 并解压后，直接运行 `Path_of_the_Unbound.exe`，无需安装。

> 本仓库包含的是游戏**编译后的 Windows 构建**（非 Unity 源码工程）。

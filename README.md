# DorokeiGame

[![Version](https://img.shields.io/badge/version-3.0-green.svg)](https://github.com/henrry/DorokeiGame/releases)
[![Minecraft](https://img.shields.io/badge/Minecraft-1.21-blue.svg)](https://www.minecraft.net/)
[![Discord](https://img.shields.io/discord/YOUR_DISCORD_ID?label=Discord&logo=discord)](https://discord.gg/zYY55dzhjd)
[![License](https://img.shields.io/badge/license-MIT-yellow.svg)](LICENSE)
[![Java](https://img.shields.io/badge/Java-21-orange.svg)](https://www.oracle.com/java/)

Advanced cops and robbers tag game plugin with visual effects and tracking systems

[English](#english) | [日本語](#日本語)

---

## English

### 🎯 Overview

DorokeiGame is an advanced cops and robbers (tag game) plugin for Minecraft servers. Players are divided into cops and robbers, with cops trying to catch all robbers before time runs out. Features include visual effects, real-time tracking, and a comprehensive lobby system.

### ✨ Key Features

#### Game Mechanics
- **Team-based gameplay** - Cops vs Robbers
- **Jail & Rescue System** - Caught players can be freed
- **Time-based Victory** - Robbers win by surviving
- **Lobby System** - Multiple concurrent games

#### Visual Effects
- **Capture Effects** - Screen darkening, particles, sounds
- **Jail Effects** - Movement debuff, visual indicators
- **Rescue Effects** - Explosion particles, speed boost
- **Tracking Particles** - Distance-based colors

#### UI Systems
- **Scoreboard** - Real-time game stats
- **Boss Bar** - Visual timer with color changes
- **Action Bar** - Distance and direction tracking
- **3D Sound** - Directional heartbeat tracking

### 📋 Commands

| Command | Description | Permission |
|---------|-------------|-----------|
| `/dorokei start` | Start a game | `dorokei.admin` |
| `/dorokei setpolice <n>` | Set cop count | `dorokei.admin` |
| `/dorokei settime <sec>` | Set duration | `dorokei.admin` |
| `/dorokei setjail` | Set jail location | `dorokei.admin` |
| `/dorokei join` | Join game | `dorokei.play` |
| `/dorokei leave` | Leave game | `dorokei.play` |

### 🚀 Installation

1. Download the latest release
2. Place in `plugins/` folder
3. Restart server
4. Configure jail: `/dorokei setjail`
5. Start playing!

### ⚙️ Configuration
```yaml
game:
  default-time: 300
  default-police: 2
  min-players: 4
  
effects:
  capture-blindness: true
  jail-particles: true
  
tracking:
  particle-trails: true
  compass-update: true
```

---

## 日本語

### 🎯 概要

DorokeiGameは、Minecraft用の高度なドロケイ（鬼ごっこ）プラグインです。プレイヤーは警官と泥棒に分かれ、警官は制限時間内に全ての泥棒を捕まえることを目指します。

### ✨ 主な機能

#### ゲームメカニクス
- **チーム戦** - 警官 vs 泥棒
- **牢獄と救出システム** - 捕まった仲間を救出可能
- **時間制限勝利** - 逃げ切れば泥棒の勝利
- **ロビーシステム** - 複数ゲーム同時進行

#### 視覚効果
- **捕獲エフェクト** - 画面暗転、パーティクル、効果音
- **牢獄エフェクト** - 移動速度低下、視覚効果
- **救出エフェクト** - 爆発パーティクル、スピードブースト
- **追跡パーティクル** - 距離に応じた色変化

#### UIシステム
- **スコアボード** - リアルタイムゲーム情報
- **ボスバー** - 色が変化するタイマー
- **アクションバー** - 距離と方向表示
- **3Dサウンド** - 心臓音による追跡

### 📋 コマンド

| コマンド | 説明 | 権限 |
|---------|------|------|
| `/dorokei start` | ゲーム開始 | `dorokei.admin` |
| `/dorokei setpolice <数>` | 警官数設定 | `dorokei.admin` |
| `/dorokei settime <秒>` | 時間設定 | `dorokei.admin` |
| `/dorokei setjail` | 牢獄設定 | `dorokei.admin` |

### 🚀 インストール

1. 最新版をダウンロード
2. `plugins/`フォルダに配置
3. サーバー再起動
4. 牢獄設定: `/dorokei setjail`
5. プレイ開始！

---

## 💬 Support

**Discord Server:** https://discord.gg/zYY55dzhjd  
**MattariMinecraft** - Japanese Minecraft Server

## 📄 License

MIT License - see [LICENSE](LICENSE) file

## 👤 Author

**henrry (へんりー)**
- MattariMinecraft Server Owner/Developer

---

<p align="center">
Made with ❤️ for MattariMinecraft<br>
© 2024 henrry. All rights reserved.
</p>
```

### GitHub Release:

**Tag:** `v3.0`

**Release title:**
```
DorokeiGame v3.0 - Lobby System & Enhanced Effects

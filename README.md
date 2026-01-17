# ドロケイゲーム v3.0

警官（鬼）と市民（泥棒）に分かれて遊ぶ、スリル満点の鬼ごっこミニゲームプラグインです。

## 🆕 v3.0 新機能

### ロビーシステム
- 複数ロビー対応（各ロビー最大20人）
- 看板クリックまたはコマンドで参加
- ロビーとゲームエリアの紐付け

### ゲームエリア管理
- pos1/pos2で矩形エリアを定義
- エリア外脱出防止
- 複数エリア作成可能

### 複数インスタンス対応
- 複数のゲームを同時実行可能
- config.ymlで設定を永続化
- サーバー再起動後も設定保持

### 警官自動割り振り
- プレイヤー数に応じて警官数を自動決定
- 2-20人に最適化されたバランス
- 30秒の逃走準備時間

---

## 📋 主要機能

### UI
- スコアボード: 残り時間、逃走中/捕獲済人数、役割
- ボスバー: 残り時間を視覚化（緑→黄→赤）
- カウントダウン演出

### 演出
- 捕獲時: 画面暗転、雷の音、パーティクル
- 牢獄内: 移動速度低下、ビーコン表示
- 救出時: 爆発エフェクト、速度上昇バフ

### 追跡システム（常時発動）
- パーティクル追跡（警官のみ表示）
- 距離で色変化（赤→黄→青）
- 方向・距離表示（8方向＋Y座標）
- 3D心臓鼓動サウンド
- コンパス更新

---

## コマンド

### セットアップコマンド（管理者用）

| コマンド | 説明 |
|---------|------|
| `/dorokei setup spawn` | 初期リスポーン地点設定 |
| `/dorokei setup lobby <ID> [名前]` | ロビー地点設定 |
| `/dorokei setup area <ID> pos1 [名前]` | エリア開始点 |
| `/dorokei setup area <ID> pos2` | エリア終了点 |
| `/dorokei setup area <ID> jail` | エリア牢獄設定 |
| `/dorokei setup link <ロビーID> <エリアID>` | 紐付け |

### プレイヤーコマンド

| コマンド | 説明 |
|---------|------|
| `/dorokei join <ロビーID>` | ロビーに参加 |
| `/dorokei leave` | ロビーから退出 |

### 管理コマンド

| コマンド | 説明 |
|---------|------|
| `/dorokei list` | ロビー・エリア一覧表示 |
| `/dorokei gamestart <ロビーID>` | ゲーム開始 |

### 旧コマンド（後方互換）

| コマンド | 説明 |
|---------|------|
| `/dorokei start` | 旧方式でゲーム開始 |
| `/dorokei setpolice <人数>` | 警官人数設定 |
| `/dorokei settime <秒数>` | ゲーム時間設定 |
| `/dorokei setjail` | 牢獄地点設定 |

**エイリアス:** `/dk`

---

## セットアップ例
```bash
# 1. リスポーン設定
/dorokei setup spawn

# 2. ロビー作成
/dorokei setup lobby lobby1 ロビー1

# 3. エリア設定
/dorokei setup area area1 pos1 エリア1
/dorokei setup area area1 pos2
/dorokei setup area area1 jail

# 4. 紐付け
/dorokei setup link lobby1 area1

# 5. 確認
/dorokei list
```

### コマンドブロック設置例
```
コマンド: /dorokei gamestart lobby1
種類: インパルス
レッドストーン: ボタンで動力供給
```

---

## 警官自動割り振り

| プレイヤー数 | 警官数 |
|-------------|--------|
| 2-4人 | 1人 |
| 5-6人 | 2人 |
| 7-8人 | 3人 |
| 9-11人 | 4人 |
| 12-14人 | 5人 |
| 15-17人 | 6人 |
| 18-20人 | 7人 |

---

## config.yml構造
```yaml
version: "3.0"

# 初期リスポーン地点
spawn-location:
  world: world
  x: 0.0
  y: 64.0
  z: 0.0

# ロビー設定
lobbies:
  lobby1:
    name: "ロビー1"
    world: world
    x: 100.0
    y: 64.0
    z: 200.0
    max-players: 20
    linked-area: area1

# ゲームエリア設定
game-areas:
  area1:
    name: "エリア1"
    world: world
    pos1: {x: 50.0, y: 0.0, z: 150.0}
    pos2: {x: 150.0, y: 256.0, z: 250.0}
    jail-location: {x: 100.0, y: 64.0, z: 200.0}

# ゲーム設定
game-settings:
  game-time: 480                    # ゲーム時間（秒）8分
  escape-preparation-time: 30       # 逃走準備時間（秒）
```

---

## 動作環境
- Spigot/Paper 1.21.x
- Java 22以上
- 依存プラグイン: なし

## コミュニティ
**Discord:** https://discord.gg/zYY55dzhjd

## ライセンス
MIT License

## 作者
へんりー

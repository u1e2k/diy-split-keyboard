# custom-split-keyboard

秋月電子 **AE-NRF52840** マイコンモジュールを搭載した、自作ワイヤレス（BLE）左右分割メカニカルキーボードの開発プロジェクトです。トラックボールを内蔵し、ファームウェアには ZMK Firmware を採用します。

---

## プロジェクトステータス (Project Status)

> **Status: `Phase 0: Preparation & Component Sourcing`**  
> 現在は部品調達およびブレッドボード上での初期プロトタイプ動作検証の準備フェーズです。

---

## 仕様概要 (Specifications)

| 項目 | 内容 |
|---|---|
| **MCU** | 秋月電子 AE-NRF52840 (Nordic nRF52840搭載 / BLE 5.0 & USB) |
| **レイアウト** | 60% 左右分割型 (カラムスタッガード または オーソリニア検討中) |
| **キースイッチ** | Cherry MX互換 (Kailhホットスワップソケット対応予定) |
| **マトリクス** | ダイオード方式 (1N4148使用) |
| **ポインティングデバイス** | トラックボールモジュール (Pimoroni Trackball / 光学式センサー等) |
| **接続方式** | Bluetooth Low Energy (BLE) / USB Type-C |
| **ファームウェア** | [ZMK Firmware](https://zmk.dev/) |
| **ハードウェア設計** | KiCad (回路図・PCB), 3D CAD (STL/STEP) |

---

## ディレクトリ構成 (Repository Structure)

```text
.
├── .gitignore                  # Git除外設定 (KiCad一時ファイル、データシートPDF等)
├── README.md                   # プロジェクト概要・ドキュメント目次
├── docs/                       # 設計・調達・技術メモ
│   ├── procurement.md          # 調達済み・購入予定パーツ一覧
│   ├── pinout.md               # AE-NRF52840のピンアサイン・マトリクス対応表
│   ├── power_circuit.md        # 電源回路・LDO・バッテリー周りの設計メモ
│   ├── trackball.md            # トラックボール用インターフェース(I2C/SPI)配線メモ
│   └── datasheets/
│       └── README.md           # 外部PDF仕様書の取得元URL一覧とダウンロード案内
├── hardware/
│   ├── kicad/                  # 回路図・PCB設計データ (KiCad)
│   └── case/                   # 3Dプリントケース・CADデータ (STL/STEP)
└── config/                     # ZMKファームウェア設定・キーマップ定義
```

---

## 開発ロードマップ (Roadmap)

- [x] **Phase 0: 部品調達・プロトタイプ検証準備** (Current)
  - [x] リポジトリ初期構成と設計ドキュメント雛形の整備
  - [x] 基本検証パーツ（ブレッドボード、ジャンパー線、ダイオード等）の調達
  - [ ] AE-NRF52840 へのブートローダー (Adafruit nRF52 Bootloader等) 書込み検証
  - [ ] ブレッドボード上での単キー/マトリクス・BLE疎通テスト
- [ ] **Phase 1: 回路・ファームウェア基礎設計**
  - [ ] 電源回路 (LDO, バッテリー充放電, 電圧監視) の選定・確定
  - [ ] トラックボール通信インターフェース (I2C/SPI) の検証
  - [ ] ZMK のシールド・ボード定義作成
- [ ] **Phase 2: PCB設計 & 試作発注**
  - [ ] KiCad での回路図作成およびPCBレイアウト設計
  - [ ] PCB製造発注 (JLCPCB / PCBWay 等)
- [ ] **Phase 3: ケース設計 & 組み立て**
  - [ ] 3Dプリントケースのモデリングと試作
  - [ ] PCB実装・はんだ付け・組み立て
  - [ ] 実機での打鍵感・トラックボール動作検証・調整

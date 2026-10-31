# データシート・仕様書管理 (Datasheets)

本ディレクトリは、回路設計やピンアサイン検討時に参照するデータシートや技術資料をローカルに保存・管理するための場所です。

> [!NOTE]
> リポジトリサイズ肥大化防止のため、PDFやZIPなどのバイナリファイルは `.gitignore` により **Git追跡から除外** されています。  
> 以下の手順またはダウンロードコマンドを利用して、各自のローカル環境にダウンロードして利用してください。

---

## 参照データシート一覧

| ファイル名 | 発行元 / 対象 | 概要・用途 | 取得元URL |
|---|---|---|---|
| `AE-NRF52840.pdf` | 秋月電子通商 | モジュール外形寸法、ピン配置、推奨電源仕様 | [akizukidenshi.com](https://akizukidenshi.com/goodsaffix/AE-NRF52840.pdf) |
| `nRF52840_PS_v1.7.pdf` | Nordic Semiconductor | nRF52840 SoC 詳細仕様書 (GPIO特性, ADC, 無線機能) | [nordicsemi.com](https://infocenter.nordicsemi.com/pdf/nRF52840_PS_v1.7.pdf) |

---

## 一括ダウンロードコマンド

本ディレクトリ（`docs/datasheets/`）に移動した上で、以下のいずれかのコマンドを実行してください。

### curl / bash の場合:
```bash
cd docs/datasheets

# AE-NRF52840 モジュール仕様書
curl -L -O https://akizukidenshi.com/goodsaffix/AE-NRF52840.pdf

# Nordic nRF52840 Product Specification
curl -L -O https://infocenter.nordicsemi.com/pdf/nRF52840_PS_v1.7.pdf
```

### PowerShell (Windows) の場合:
```powershell
Set-Location docs/datasheets
Invoke-WebRequest -Uri "https://akizukidenshi.com/goodsaffix/AE-NRF52840.pdf" -OutFile "AE-NRF52840.pdf"
Invoke-WebRequest -Uri "https://infocenter.nordicsemi.com/pdf/nRF52840_PS_v1.7.pdf" -OutFile "nRF52840_PS_v1.7.pdf"
```


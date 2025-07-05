# Marp DigiOn カスタムテーマ

DigiOn向けのMarpプレゼンテーション用カスタムテーマです。

## 概要

このリポジトリには、DigiOnのブランドガイドラインに沿ったMarp用のカスタムCSSテーマが含まれています。タイトルスライド、通常スライド、最終スライドそれぞれに適切なスタイルが定義されています。

## クイックスタート

GitHub経由で直接テーマを使用できます（ローカルファイル不要）：

```yaml
---
marp: true
style: |
  @import url('https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fixed.css');
---

# プレゼンテーションタイトル
```

## 特徴

- **タイトルスライド**: DigiOnロゴとCONFIDENTIAL表記を含む
- **通常スライド**: 赤いアクセントカラーを使用した見出し
- **最終スライド**: 会社情報表示用のレイアウト
- **フォント**: Noto Sans JPを使用した読みやすいデザイン

## ファイル構成

```
marp-digion-template/
├── assets/
│   ├── marp-custom.css         # オリジナルのカスタムテーマ
│   ├── marp-custom-fixed.css   # 修正版テーマ（HD: 1280×720）
│   ├── marp-custom-fullhd.css  # FullHD版テーマ（1920×1080）
│   ├── image1.png              # DigiOnロゴ
│   ├── image2.png              # CONFIDENTIAL表記
│   ├── image3.jpg              # 背景画像
│   ├── image4.jpg              # タイトルスライド背景
│   └── image5.jpg              # 最終スライド背景
├── sample/
│   ├── basic-presentation.md   # 基本的な使用例
│   ├── fullhd-presentation.md  # FullHD版の使用例
│   ├── advanced-features.md    # 高度な機能の使用例
│   └── README.md               # サンプルの説明
├── .marprc.yml                 # Marp CLI設定ファイル
└── README.md                   # このファイル
```

## 使用方法

### 1. テーマの適用

#### 方法A: GitHub経由（推奨）

```yaml
---
marp: true
style: |
  @import url('https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fixed.css');
---
```

#### 方法B: ローカルファイル

```yaml
---
marp: true
theme: ./assets/marp-custom-fixed.css
---
```

### 2. スライドクラスの使用

#### タイトルスライド

```markdown
<!-- _class: title -->

# プレゼンテーションタイトル
サブタイトル

<div class="date">2025年1月15日</div>
<div class="info">資料種別：社内資料</div>
<div class="version">Ver.1.0</div>
<div class="company">株式会社DigiOn</div>
```

#### 通常スライド

```markdown
## スライドタイトル

- 箇条書き項目1
- 箇条書き項目2
- 箇条書き項目3
```

#### 最終スライド

```markdown
<!-- _class: end -->

<div class="addresses">
  <div class="address">
    <h3>本社</h3>
    〒102-0084<br>
    東京都千代田区二番町3-5<br>
    麹町三葉ビル
  </div>
  <div class="address">
    <h3>福岡オフィス</h3>
    〒812-0011<br>
    福岡県福岡市博多区博多駅前2-20-1<br>
    大博多ビル
  </div>
</div>
```

## カスタマイズ

CSSファイルを編集することで、以下の要素をカスタマイズできます：

- **カラーテーマ**: アクセントカラー（デフォルト: #E60012）
- **フォントサイズ**: 見出しや本文のサイズ
- **余白**: スライドのパディングやマージン
- **背景画像**: 各スライドタイプの背景

## 注意事項

- 画像ファイルはGitHub上の raw URLを参照しています
- プライベートリポジトリの場合は、適切なアクセス権限が必要です
- CONFIDENTIALマークが含まれているため、社外への公開時は注意してください

## ライセンス

社内利用限定
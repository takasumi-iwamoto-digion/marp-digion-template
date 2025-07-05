# Marp DigiOn カスタムテーマ

DigiOn向けのMarpプレゼンテーション用カスタムテーマです。

## 概要

このリポジトリには、DigiOnのブランドガイドラインに沿ったMarp用のカスタムCSSテーマが含まれています。タイトルスライド、通常スライド、最終スライドそれぞれに適切なスタイルが定義されています。

## クイックスタート

シンプルな構成で、すぐに使い始められます：

```yaml
---
marp: true
theme: ./marp-custom-fixed.css
---

# プレゼンテーションタイトル
```

VS Code、Marp CLI、どちらでも同じパスで動作します。

## 特徴

- **タイトルスライド**: DigiOnロゴとCONFIDENTIAL表記を含む
- **通常スライド**: 赤いアクセントカラーを使用した見出し
- **最終スライド**: 会社情報表示用のレイアウト
- **フォント**: Noto Sans JPを使用した読みやすいデザイン

## ファイル構成

```
marp-digion-template/
├── marp-custom-fixed.css        # カスタムテーマ（HD: 1280×720）
├── basic-presentation.md        # 基本的な使用例（ローカル版）
├── basic-presentation-github.md # GitHub経由版の使用例
├── images/                      # 画像ディレクトリ
│   ├── image1.png              # DigiOnロゴ
│   ├── image2.png              # CONFIDENTIAL表記
│   ├── image3.jpg              # 背景画像
│   ├── image4.jpg              # タイトルスライド背景
│   └── image5.jpg              # 最終スライド背景
├── docs/                        # ドキュメント
│   ├── github-hosting-guide.md
│   ├── vscode-setup-guide.md
│   └── ...
├── .vscode/                     # VS Code設定
│   └── settings.json
├── .marprc.yml                  # Marp CLI設定ファイル
└── README.md                    # このファイル
```

## 使用方法

### 1. テーマの適用

#### 方法A: ローカル版（開発・オフライン用）

```yaml
---
marp: true
theme: ./marp-custom-fixed.css
---
```

#### 方法B: GitHub経由（配布・共有用）

```yaml
---
marp: true
style: |
  @import url('https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/marp-custom-fixed.css');
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
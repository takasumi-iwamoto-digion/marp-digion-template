# サンプルプレゼンテーション

このディレクトリには、GitHub経由でDigiOnカスタムテーマを適用したMarpプレゼンテーションのサンプルが含まれています。

## サンプルファイル

### 1. basic-presentation.md
- 基本的なプレゼンテーションの例
- HD解像度（1280×720）
- GitHub経由でのテーマ読み込み方法を説明

### 2. fullhd-presentation.md
- FullHD解像度（1920×1080）のサンプル
- 大型ディスプレイ向けの高解像度版
- HD版との違いを説明

### 3. advanced-features.md
- Marpの高度な機能を活用した例
- トランジション効果
- フラグメント化されたリスト
- 複数背景、コードブロック、テーブル、数式

## 使用方法

### 1. プレビュー（サーバーモード）

```bash
# 基本的なプレゼンテーションをプレビュー
marp -s basic-presentation.md

# FullHD版をプレビュー
marp -s fullhd-presentation.md

# 高度な機能のデモをプレビュー
marp -s advanced-features.md
```

### 2. HTML出力

```bash
# HTMLファイルとして出力
marp basic-presentation.md -o basic-presentation.html
```

### 3. PDF出力

```bash
# PDFとして出力（プレゼンターノート付き）
marp --pdf --pdf-notes basic-presentation.md -o basic-presentation.pdf

# PDFアウトライン（しおり）付き
marp --pdf --pdf-outlines basic-presentation.md
```

### 4. PowerPoint出力

```bash
# PPTXファイルとして出力
marp --pptx basic-presentation.md -o basic-presentation.pptx
```

## 注意事項

### インターネット接続が必要
これらのサンプルはGitHub経由でテーマを読み込むため、インターネット接続が必要です。

### オフライン使用の場合
オフラインで使用する場合は、以下のようにローカルテーマを参照してください：

```yaml
---
marp: true
theme: ../assets/marp-custom-fixed.css
---
```

## カスタマイズ

### テーマの切り替え

```yaml
# HD版（標準）
style: |
  @import url('https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fixed.css');

# FullHD版
style: |
  @import url('https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fullhd.css');
```

### トランジション効果

```yaml
transition: fade    # フェード効果
transition: slide   # スライド効果
transition: cover   # カバー効果
```

### プレゼンタービュー
- `p`キーでプレゼンタービューを開く
- HTMLコメントがプレゼンターノートとして表示される

## トラブルシューティング

### テーマが読み込まれない場合

1. インターネット接続を確認
2. GitHubのURLが正しいか確認
3. リポジトリがpublicになっているか確認

### 画像が表示されない場合

1. 画像URLが正しいか確認
2. GitHub上に画像ファイルが存在するか確認

## 参考リンク

- [Marp公式サイト](https://marp.app/)
- [Marp CLI ドキュメント](https://github.com/marp-team/marp-cli)
- [DigiOnテーマリポジトリ](https://github.com/takasumi-iwamoto-digion/marp-digion-template)
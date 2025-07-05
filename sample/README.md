# サンプルプレゼンテーション

このディレクトリには、DigiOnカスタムテーマを適用したMarpプレゼンテーションのサンプルが含まれています。**GitHub版（本番用）**と**ローカル版（開発用）**の両方を用意しています。

## サンプルファイル

### GitHub版（本番用）- インターネット接続必要

#### 1. basic-presentation-github.md
- 基本的なプレゼンテーションの例
- HD解像度（1280×720）
- GitHub経由でのテーマ読み込み

#### 2. advanced-features-github.md
- Marpの高度な機能を活用した例
- トランジション効果、フラグメント化されたリスト等

### ローカル版（開発用）- オフライン対応

#### 1. basic-presentation-local.md
- 基本的なプレゼンテーションの例（ローカルCSS使用）
- 開発・テスト用

#### 2. advanced-features-local.md
- 高度な機能のデモ（ローカルCSS使用）
- カスタマイズ実験用

## 使用方法

### 1. プレビュー（サーバーモード）

#### GitHub版（本番確認用）
```bash
# 基本的なプレゼンテーション
marp -s basic-presentation-github.md

# 高度な機能のデモ
marp -s advanced-features-github.md
```

#### ローカル版（開発用）
```bash
# ウォッチモードで起動（CSS変更が即反映）
marp -w -s basic-presentation-local.md

# 全ファイルを監視
marp -w -s .
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

## GitHub版とローカル版の使い分け

### GitHub版を使用する場合
- **本番プレゼンテーション**：最終的な発表時
- **チーム共有**：URLを共有するだけで利用可能
- **配布資料**：常に最新版のテーマを適用

### ローカル版を使用する場合
- **テーマ開発**：CSSの編集・カスタマイズ時
- **オフライン環境**：インターネット接続がない場所
- **高速プレビュー**：ネットワーク遅延なし

## 開発ワークフロー

1. **開発フェーズ**
   - ローカル版でCSSを編集
   - ウォッチモードで変更を確認
   ```bash
   marp -w -s advanced-features-local.md
   ```

2. **テストフェーズ**
   - 編集したCSSの動作確認
   - 複数の解像度でテスト

3. **デプロイフェーズ**
   - GitHubへプッシュ
   - GitHub版で最終確認
   ```bash
   marp -s advanced-features-github.md
   ```

## カスタマイズ

### テーマの切り替え

```yaml
# HD版（1280×720）
style: |
  @import url('https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fixed.css');
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
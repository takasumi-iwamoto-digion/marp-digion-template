# 画像使用ガイド

## 画像が表示されない場合の対処法

### 問題

Marp CLIでPDF/PNG出力時に、CSSで指定した背景画像（ロゴなど）が表示されない。

### 原因

セキュリティ上の理由により、デフォルトではローカルファイルへのアクセスが制限されています。

### 解決方法

#### 1. コマンドラインオプションを使用

```bash
# PDF出力（画像を含む）
marp --allow-local-files --pdf basic-presentation.md

# PNG出力（画像を含む）
marp --allow-local-files --images png basic-presentation.md

# PowerPoint出力（画像を含む）
marp --allow-local-files --pptx basic-presentation.md
```

#### 2. 設定ファイルで有効化

`.marprc.yml`で常に有効にする：

```yaml
allowLocalFiles: true
```

⚠️ **セキュリティ警告**: `--allow-local-files`を有効にすると、信頼できないMarkdownファイルがローカルファイルにアクセスできるようになります。自分で作成したファイルのみで使用してください。

## サーバーモードでの画像表示

サーバーモード（`marp -s`）では、画像は正常に表示されます：

```bash
marp -s basic-presentation.md
```

## GitHub版での画像

GitHub版（`basic-presentation-github.md`）では、画像URLがGitHub経由になるため、この問題は発生しません。

## トラブルシューティング

### 画像パスの確認

CSSファイル内の画像パス：

```css
background-image: url('../assets/logo.png');
```

画像ファイルの配置：

```
marp-digion-template/
├── theme/
│   └── marp-theme-digion.css
├── assets/
│   ├── logo.png
│   └── ...
```

### HTMLでは表示されるがPDF/PNGで表示されない場合

これは正常な動作です。`--allow-local-files`オプションを追加してください。

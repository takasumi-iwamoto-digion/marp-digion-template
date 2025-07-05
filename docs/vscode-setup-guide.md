# VS Code Marp拡張機能設定ガイド

## 問題と解決策

VS CodeのMarp拡張機能では、相対パスの解決方法がMarp CLIと異なるため、カスタムCSSが正しく読み込まれない場合があります。

## 設定方法

### 1. VS Code設定ファイルの作成

`.vscode/settings.json`を作成し、以下の内容を記述：

```json
{
  "markdown.marp.themes": [
    "./assets/marp-custom-fixed.css"
  ],
  "markdown.marp.enableHtml": true
}
```

### 2. Markdownファイルでの指定方法

#### 方法A: テーマ名で指定（推奨）
```yaml
---
marp: true
theme: marp-custom-fixed
---
```

#### 方法B: 相対パスで指定
```yaml
---
marp: true
theme: ./assets/marp-custom-fixed.css
---
```

## 環境別の使い分け

| 環境 | ファイル | テーマ指定方法 |
|------|----------|----------------|
| VS Code プレビュー | basic-presentation-vscode.md | `theme: marp-custom-fixed` |
| Marp CLI（開発） | basic-presentation-local.md | `theme: ../assets/marp-custom-fixed.css` |
| 本番（GitHub） | basic-presentation-github.md | `style: @import url(...)` |

## トラブルシューティング

### CSSが適用されない場合

1. **VS Codeを再起動**
   - 設定ファイルの変更後は再起動が必要な場合があります

2. **パスの確認**
   - ワークスペースのルートディレクトリを確認
   - `.vscode/settings.json`の相対パスを調整

3. **Marp拡張機能の確認**
   - 最新版がインストールされているか確認
   - 拡張機能の設定でHTMLが有効になっているか確認

### デバッグ方法

1. **開発者ツールを開く**
   - `Ctrl+Shift+I` (Mac: `Cmd+Shift+I`)
   - コンソールでエラーを確認

2. **出力パネルを確認**
   - 表示 → 出力 → Marp

## 推奨ワークフロー

1. **開発時**
   - VS Code: `basic-presentation-vscode.md`でプレビュー
   - ターミナル: `marp -w -s basic-presentation-local.md`で詳細確認

2. **共有時**
   - GitHub版（`basic-presentation-github.md`）を使用

3. **プレゼン時**
   - 事前にHTML/PDFに変換
   - オフライン環境に備える
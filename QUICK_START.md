# クイックスタートガイド

## 1. 新しいプレゼンテーションの作成

新規ファイル（例：`my-presentation.md`）を作成し、以下を記述：

```yaml
---
marp: true
theme: ./marp-custom-fixed.css
---

# プレゼンテーションタイトル
```

## 2. プレビュー方法

### VS Code
1. ファイルを開く
2. `Ctrl+K V` (Mac: `Cmd+K V`)

### Marp CLI
```bash
marp -s my-presentation.md
```

## 3. 出力方法

```bash
# HTML
marp my-presentation.md

# PDF（画像を含む場合）
marp --allow-local-files --pdf my-presentation.md

# PNG画像（画像を含む場合）
marp --allow-local-files --images png my-presentation.md

# PowerPoint
marp --allow-local-files --pptx my-presentation.md
```

## それだけです！

パスの問題に悩む必要はもうありません。すべての環境で同じパス（`./marp-custom-fixed.css`）が使えます。
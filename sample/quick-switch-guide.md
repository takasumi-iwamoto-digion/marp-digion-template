# GitHub版とローカル版の簡単切り替えガイド

## 切り替え方法

### GitHub版 → ローカル版

```yaml
# 変更前（GitHub版）
style: |
  @import url('https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fixed.css');

# 変更後（ローカル版）
theme: ../assets/marp-custom-fixed.css
```

### ローカル版 → GitHub版

```yaml
# 変更前（ローカル版）
theme: ../assets/marp-custom-fixed.css

# 変更後（GitHub版）
style: |
  @import url('https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fixed.css');
```

## VSCodeでの一括置換

1. `Ctrl+Shift+H`（Mac: `Cmd+Shift+H`）で置換パネルを開く
2. 正規表現モードをON（`.*`ボタン）
3. 以下のパターンで置換：

### GitHub版へ切り替え
- 検索: `theme: ../assets/(marp-custom-fixed\.css)`
- 置換: `style: |\n  @import url('https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/$1');`

### ローカル版へ切り替え
- 検索: `style: \|\n\s+@import url\('https://raw\.githubusercontent\.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/(marp-custom-fixed\.css)'\);`
- 置換: `theme: ../assets/$1`

## スクリプトでの切り替え（bash）

```bash
#!/bin/bash
# switch-to-github.sh

for file in *.md; do
  sed -i 's|theme: ../assets/\(marp-custom-[^.]*\.css\)|style: |\
  @import url('\''https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/\1'\'');|g' "$file"
done
```

```bash
#!/bin/bash
# switch-to-local.sh

for file in *.md; do
  sed -i '/style: |/,/@import url/ {
    s|style: |\s*@import url('\''https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/\(marp-custom-[^'\'']*\.css\)'\'');|theme: ../assets/\1|
  }' "$file"
done
```
# HD vs FullHD サイズ比較ガイド

## サイズ比較

| 項目 | HD (1280x720) | FullHD (1920x1080) | 変化率 |
|------|---------------|-------------------|--------|
| 解像度 | 921,600px | 2,073,600px | 2.25倍 |
| アスペクト比 | 16:9 | 16:9 | 同じ |
| 基本フォントサイズ | 32px | 48px | 1.5倍 |
| ファイルサイズ（PDF） | 約1-2MB | 約2-5MB | 約2倍 |

## 推奨される使い分け

### HD版（marp-custom-fixed.css）を使用する場合
- 社内の標準的な会議室での発表
- Web会議での画面共有
- 古いプロジェクター環境
- ファイルサイズを抑えたい場合

### FullHD版（marp-custom-fullhd.css）を使用する場合
- 大型ディスプレイでの発表
- 高解像度プロジェクター環境
- 印刷物として配布する場合
- 詳細な図表を含む資料

## 使用方法

```yaml
# HD版を使用
---
marp: true
theme: digion
---

# FullHD版を使用
---
marp: true
theme: digion-fullhd
---
```

## 両方のテーマを登録する方法

```bash
# Marp CLIでの使用
marp --theme-set ./assets/marp-custom-fixed.css ./assets/marp-custom-fullhd.css presentation.md

# 設定ファイルでの指定（.marprc.yml）
themeSet:
  - ./assets/marp-custom-fixed.css
  - ./assets/marp-custom-fullhd.css
```
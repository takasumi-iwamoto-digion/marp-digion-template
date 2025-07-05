# Marp最新機能調査レポート

## 概要

DigiOnカスタムテーマの現状分析と、最新のMarp機能を活用した改善提案をまとめました。

## 現在のテーマの修正が必要な点

### 1. CSSメタデータの追加
```css
/* @theme digion */
```
テーマCSSの先頭に必ず追加する必要があります。

### 2. スライドサイズの定義
```css
:root {
  width: 1280px;
  height: 720px;
  font-size: 32px;
}
```

### 3. 画像参照の修正
- `image1.jpg` → `image1.png`に修正（140行目）

## 最新Marp機能の活用提案

### 1. スライドトランジション（View Transition API）

Marp CLIの最新版では、スライド間のトランジション効果がサポートされています。

```yaml
---
transition: fade
---
```

利用可能なトランジション：
- `fade`: フェード効果
- `slide`: スライド効果
- `cover`: カバー効果
- カスタムトランジションも定義可能

### 2. プレゼンターノート

HTMLコメントとして記述したプレゼンターノートが、`p`キーで開くプレゼンタービューに表示されます。

```markdown
<!-- プレゼンターノート：ここに話す内容を記載 -->
```

### 3. フラグメント化されたリスト

箇条書きを段階的に表示する機能：

```markdown
* 最初に表示される項目
* 次に表示される項目
* 最後に表示される項目
```

### 4. プログレスバー

bespokeテンプレートでプログレスバーを表示：

```bash
marp --bespoke.progress slide.md
```

### 5. 高度な画像配置

分割背景やフィルター機能：

```markdown
![bg left:40%](image.jpg)
![brightness:.8 sepia:50%](image.jpg)
```

### 6. PDF/PPTXへの変換時の機能

- PDF注釈としてのプレゼンターノート
- PDFアウトライン（しおり）
- 編集可能なPPTX生成（実験的機能）

## 推奨される改善実装

### 1. 修正版CSS（marp-theme-digion.css）

```css
/* @theme digion */

:root {
  width: 1280px;
  height: 720px;
  font-size: 32px;
}

section {
  font-family: 'Noto Sans JP', 'Hiragino Sans', sans-serif;
  color: #333333;
  background-color: #ffffff;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  padding-top: 150px;
}

/* 以下、既存のスタイルを継続... */
```

### 2. 使用例の更新

```yaml
---
marp: true
theme: digion
transition: fade
paginate: true
---

<!-- _class: title -->

# プレゼンテーションタイトル
サブタイトル

<div class="date">2025年1月15日</div>
<div class="info">資料種別：社内資料</div>
<div class="version">Ver.1.0</div>
<div class="company">株式会社DigiOn</div>

<!-- ここにプレゼンターノートを記載 -->

---

## アジェンダ

* 最初のトピック
* 次のトピック
* 最後のトピック

---

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

## 推奨コマンド

### 開発時のプレビュー
```bash
marp -w -s --bespoke.progress presentation.md
```

### PDF生成（プレゼンターノート付き）
```bash
marp --pdf --pdf-notes presentation.md
```

### PPTX生成
```bash
marp --pptx presentation.md
```

## まとめ

現在のDigiOnテーマは基本的な構造は良好ですが、最新のMarp機能を活用することで、より洗練されたプレゼンテーション体験を提供できます。特にトランジション機能とプレゼンターノート機能は、プレゼンテーションの品質向上に大きく貢献するでしょう。
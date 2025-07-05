---
marp: true
style: |
  @import url('https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fixed.css');
transition: fade
paginate: true
---

<!-- _class: title -->
<!-- _paginate: false -->

# Marp高度な機能デモ
トランジションとフラグメントの活用

<div class="date">2025年1月15日</div>
<div class="info">資料種別：機能デモ</div>
<div class="version">Ver.1.0</div>
<div class="company">株式会社DigiOn</div>

<!--
このプレゼンテーションでは、
Marpの高度な機能を実際に体験できます。
pキーでプレゼンタービューを開いてみてください。
-->

---

<!-- transition: cover -->

## トランジション効果の変更

このスライドは`cover`トランジションを使用しています

### 利用可能なトランジション

* `fade` - フェード効果（デフォルト）
* `slide` - スライド効果
* `cover` - カバー効果
* カスタムトランジション（CSS定義）

<!--
トランジションはスライドごとに
変更することができます。
適切に使い分けることで、
プレゼンテーションに動きを加えられます。
-->

---

<!-- transition: slide -->

## フラグメント化されたリスト

以下の項目が順番に表示されます：

* DigiOnの主要製品ラインナップ
* 映像・音声処理技術の強み
* クロスプラットフォーム対応
* 高い技術力と豊富な実績
* お客様からの信頼

<!--
フラグメント機能により、
話の流れに合わせて
情報を段階的に開示できます。
クリックまたはスペースキーで進めてください。
-->

---

## 複数背景の活用

![bg vertical](https://fakeimg.pl/800x600/0288d1/fff/?text=DigiOn)
![bg](https://fakeimg.pl/800x600/02669d/fff/?text=Technology)
![bg](https://fakeimg.pl/800x600/67b8e3/fff/?text=Innovation)

### 垂直配置の背景画像

右側に3つの画像を垂直に配置しています

<!--
複数の背景画像を組み合わせることで、
視覚的に印象的なスライドを作成できます。
-->

---

## コードブロックの表示

プログラムコードも美しく表示されます：

```javascript
// Marpの設定例
const config = {
  engine: '@marp-team/marpit',
  theme: 'digion',
  options: {
    html: true,
    pdf: {
      notes: true,
      outlines: true
    }
  }
};
```

<!--
コードブロックは自動的に
シンタックスハイライトされ、
技術プレゼンテーションに最適です。
-->

---

## テーブルの活用

| 機能 | HD版 | FullHD版 | 推奨用途 |
|------|------|----------|----------|
| 解像度 | 1280×720 | 1920×1080 | - |
| フォントサイズ | 32px | 48px | - |
| 会議室プロジェクター | ◎ | ○ | HD版推奨 |
| 大型ディスプレイ | ○ | ◎ | FullHD版推奨 |
| ファイルサイズ | 小 | 大 | 用途に応じて |

<!--
テーブルも見やすくスタイリングされ、
比較データの表示に便利です。
-->

---

## 数式の表示（LaTeX）

Marpは数式の表示にも対応しています：

$$
E = mc^2
$$

インライン数式も可能です：$a^2 + b^2 = c^2$

<!--
技術文書や学術プレゼンテーションで
数式を美しく表示できます。
-->

---

<!-- _class: end -->
<!-- _paginate: false -->

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
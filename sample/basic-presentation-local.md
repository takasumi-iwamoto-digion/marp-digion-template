---
marp: true
theme: ../assets/marp-custom-fixed.css
transition: fade
paginate: true
---

<!-- _class: title -->
<!-- _paginate: false -->

# DigiOn プレゼンテーション
ローカルテーマを適用したサンプル（開発用）

<div class="date">2025年1月15日</div>
<div class="info">資料種別：デモ資料</div>
<div class="version">Ver.1.0</div>
<div class="company">株式会社DigiOn</div>

<!--
このスライドはローカルのCSSファイルを読み込んでいます。
開発・テスト時に使用してください。
-->

---

## ローカル版の使用方法

このプレゼンテーションは以下の特徴があります：

- CSSテーマをローカルファイルから読み込み
- 開発中の変更が即座に反映
- インターネット接続不要
- オフライン環境でも使用可能

---

## 必要な設定

Markdownファイルの冒頭に以下を記述：

```yaml
---
marp: true
theme: ../assets/marp-custom-fixed.css
---
```

相対パスでローカルのCSSファイルを指定します。

---

## 開発ワークフロー

1. **CSSの編集**
   ```bash
   # テーマCSSを編集
   code ../assets/marp-custom-fixed.css
   ```

2. **プレビュー確認**
   ```bash
   # ウォッチモードで起動
   marp -w -s basic-presentation-local.md
   ```

3. **変更が即座に反映**

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
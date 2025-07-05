---
marp: true
style: |
  @import url('https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fixed.css');
transition: fade
paginate: true
---

<!-- _class: title -->
<!-- _paginate: false -->

# DigiOn プレゼンテーション
GitHub経由でテーマを適用したサンプル

<div class="date">2025年1月15日</div>
<div class="info">資料種別：デモ資料</div>
<div class="version">Ver.1.0</div>
<div class="company">株式会社DigiOn</div>

<!--
このスライドはGitHub経由でカスタムテーマを読み込んでいます。
ローカルにCSSファイルは必要ありません。
-->

---

## GitHub経由でのテーマ適用

このプレゼンテーションは以下の特徴があります：

- CSSテーマをGitHubから直接読み込み
- 画像リソースもGitHub経由で参照
- ローカルファイル不要で利用可能
- チーム全体で同じテーマを共有

---

## 必要な設定

Markdownファイルの冒頭に以下を記述するだけ：

```yaml
---
marp: true
style: |
  @import url('https://raw.githubusercontent.com/
    takasumi-iwamoto-digion/marp-digion-template/
    main/assets/marp-custom-fixed.css');
---
```

---

## コマンドライン実行例

```bash
# HTMLに変換
marp basic-presentation.md

# PDFに変換（プレゼンターノート付き）
marp --pdf --pdf-notes basic-presentation.md

# サーバーモードで確認
marp -s basic-presentation.md
```

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
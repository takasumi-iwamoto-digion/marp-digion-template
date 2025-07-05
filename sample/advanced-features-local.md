---
marp: true
theme: ../assets/marp-custom-fixed.css
transition: fade
paginate: true
---

<!-- _class: title -->
<!-- _paginate: false -->

# Marp高度な機能デモ
ローカルテーマ版（開発用）

<div class="date">2025年1月15日</div>
<div class="info">資料種別：機能デモ</div>
<div class="version">Ver.1.0</div>
<div class="company">株式会社DigiOn</div>

<!--
ローカル版では、CSSのカスタマイズを
リアルタイムでテストできます。
-->

---

<!-- transition: cover -->

## CSSカスタマイズの例

ローカル版では以下のような実験が可能：

### スタイルの調整

* カラーテーマの変更
* フォントサイズの微調整
* アニメーション効果の追加
* レイアウトの改善

<!--
開発者ツールを使用して、
その場でCSSを編集・確認できます。
-->

---

<!-- transition: slide -->

## 画像パスの違い

### GitHub版
```markdown
![bg](https://github.com/.../image.jpg?raw=true)
```

### ローカル版
```markdown
![bg](../assets/image.jpg)
```

相対パスで直接参照できます。

---

## 開発用ツール

```bash
# ウォッチモードでサーバー起動
marp -w -s advanced-features-local.md

# 複数ファイルを同時監視
marp -w -s .

# ブラウザを指定して起動
marp -s --browser chrome advanced-features-local.md
```

<!--
ウォッチモードを使うことで、
ファイル保存時に自動的に
ブラウザがリロードされます。
-->

---

## CSS変更の即時確認

1. テキストエディタでCSSを編集
2. 保存（Ctrl+S / Cmd+S）
3. ブラウザが自動リロード
4. 変更内容を即座に確認

### 便利な開発環境

* VSCode + Marp拡張
* ブラウザの開発者ツール
* デュアルモニター推奨

---

## カスタムCSSの追加例

```css
/* カスタムアニメーション */
@keyframes slideIn {
  from { transform: translateX(-100%); }
  to { transform: translateX(0); }
}

section h2 {
  animation: slideIn 0.5s ease-out;
}
```

---

## デバッグのヒント

![bg right:40%](../assets/image3.jpg)

### ブラウザ開発者ツール

- **要素の検証**: 右クリック→検証
- **CSSの確認**: Stylesパネル
- **レスポンシブ**: デバイスモード
- **コンソール**: エラー確認

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
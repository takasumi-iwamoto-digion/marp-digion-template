---
marp: true
theme: ./marp-custom-fixed.css
transition: fade
paginate: true
---

<!-- _class: title -->
<!-- _paginate: false -->

# DigiOn 高度なレイアウト例
target/のデザイン目標を実現するサンプル

<div class="date">2025年1月15日</div>
<div class="info">資料種別：レイアウトデモ</div>
<div class="version">Ver.1.0</div>
<div class="company">株式会社DigiOn</div>

---

## 通常のスライド（default）

これは通常のスライドレイアウトです。`target/DigiOn-Template-default.png`のデザインを再現しています。

- 赤いアクセントカラーの見出し
- 標準的な箇条書きスタイル
- ページ番号の表示

---

## 見出しスライド（headline）

大きな見出しのみのスライドです。

セクションの区切りや、重要なメッセージの強調に使用します。

`target/DigiOn-Template-headline.png`のスタイルを参考にしています。

---

![bg left:40%](./images/image3.jpg)

## 左画像レイアウト（half-left）

左側に画像を配置したレイアウトです。

`target/DigiOn-Template-half-left.png`のデザインを実現しています。

- 画像とテキストのバランス
- 視覚的な説明に最適
- コンテンツエリアは右側に集約

---

![bg right:40%](./images/image3.jpg)

## 右画像レイアウト（half-right）

右側に画像を配置したレイアウトです。

`target/DigiOn-Template-half-right.png`のデザインを実現しています。

### 使用例
- 製品の紹介
- 技術の説明
- ビジュアル重視のコンテンツ

---

## フラグメント機能

順番に表示される箇条書き：

* DigiOnの強み
* 高度な映像・音声処理技術
* クロスプラットフォーム対応
* 豊富な実績と信頼

---

## コードブロックの例

```javascript
// DigiOn SDK の使用例
const digion = new DigiOnSDK({
  apiKey: 'your-api-key',
  platform: 'web'
});

digion.initialize().then(() => {
  console.log('DigiOn SDK initialized');
});
```

---

## テーブルレイアウト

| 製品名 | 対応OS | 主な機能 |
|--------|--------|----------|
| DigiOn Video | Windows/Mac/Linux | 動画再生・編集 |
| DigiOn Audio | iOS/Android | 音声処理・変換 |
| DigiOn Stream | Web | ストリーミング配信 |

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
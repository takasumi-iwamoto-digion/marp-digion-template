# ロゴ・CONFIDENTIAL画像表示の解決方法

## 問題
CSS疑似要素（`::before`, `::after`）で設定した背景画像が、Marp CLIでのPDF/PNG出力時に表示されない。

## 原因
Marpの変換エンジンは、CSS疑似要素の背景画像を正しくレンダリングできない場合があります。特にPDF/PNG出力時に問題が発生します。

## 解決方法

### 推奨: Markdown内に直接画像を挿入

タイトルスライドの例：
```markdown
<!-- _class: title -->

<img src="./images/image1.png" class="logo" alt="DigiOn">
<img src="./images/image2.png" class="confidential" alt="CONFIDENTIAL">

# プレゼンテーションタイトル
```

最終スライドの例：
```markdown
<!-- _class: end -->

<img src="./images/image1.png" class="logo" alt="DigiOn">

<div class="addresses">
  ...
</div>
```

### CSSでの位置調整

```css
section.title img.logo {
  position: absolute;
  top: 30px;
  left: 50px;
  width: 150px;
  height: auto;
}

section.title img.confidential {
  position: absolute;
  top: 30px;
  right: 50px;
  width: 150px;
  height: auto;
}
```

## メリット

1. **確実な表示**: すべての出力形式（HTML/PDF/PNG/PPTX）で確実に表示される
2. **デバッグが容易**: 画像が表示されない場合、パスの問題だとすぐわかる
3. **柔軟性**: 必要に応じて画像を変更しやすい

## 注意点

- 必ず `--allow-local-files` オプションを使用する
- 画像パスは相対パスで指定する
- classを使用してCSSでスタイリングする
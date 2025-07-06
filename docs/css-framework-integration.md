# CSSフレームワーク統合ガイド

MarpでBootstrapやTailwind CSSなどのCSSフレームワークを使用する方法を説明します。

## Tailwind CSS統合

### 基本的な使い方

```markdown
---
marp: true
theme: digion
---

<script src="https://cdn.tailwindcss.com/3.4.0"></script>
<script>
tailwind.config = { 
  corePlugins: { 
    preflight: false  // Marpのデフォルトスタイルとの競合を防ぐ
  } 
}
</script>

## Tailwindクラスを使用したレイアウト

<div class="grid grid-cols-2 gap-4">
  <div class="bg-gray-100 p-4 rounded">
    <h3 class="text-red-600 font-bold">左カラム</h3>
    <p class="text-sm">Tailwindのグリッドシステム</p>
  </div>
  <div class="bg-gray-100 p-4 rounded">
    <h3 class="text-red-600 font-bold">右カラム</h3>
    <p class="text-sm">簡単にレスポンシブ対応</p>
  </div>
</div>
```

### 利用可能なTailwindクラス例

```markdown
<!-- 3カラムグリッド -->
<div class="grid grid-cols-3 gap-6">
  <div class="col-span-1">カラム1</div>
  <div class="col-span-1">カラム2</div>
  <div class="col-span-1">カラム3</div>
</div>

<!-- フレックスボックス -->
<div class="flex justify-between items-center">
  <div class="flex-1">左</div>
  <div class="flex-1">中央</div>
  <div class="flex-1">右</div>
</div>

<!-- カード風レイアウト -->
<div class="bg-white shadow-lg rounded-lg p-6">
  <h3 class="text-xl font-semibold mb-2">カードタイトル</h3>
  <p class="text-gray-600">カードの内容</p>
</div>
```

## Bootstrap統合

### 基本的な使い方

```markdown
---
marp: true
theme: digion
style: |
  @import url('https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css');
---

## Bootstrapグリッドシステム

<div class="container-fluid">
  <div class="row">
    <div class="col-md-6">
      <h3>左カラム</h3>
      <p>Bootstrapの12カラムグリッド</p>
    </div>
    <div class="col-md-6">
      <h3>右カラム</h3>
      <p>レスポンシブ対応</p>
    </div>
  </div>
</div>
```

### 利用可能なBootstrapクラス例

```markdown
<!-- アラート -->
<div class="alert alert-primary" role="alert">
  重要なお知らせ
</div>

<!-- カード -->
<div class="card" style="width: 18rem;">
  <div class="card-body">
    <h5 class="card-title">カードタイトル</h5>
    <p class="card-text">カードの内容</p>
  </div>
</div>

<!-- プログレスバー -->
<div class="progress">
  <div class="progress-bar" role="progressbar" style="width: 75%"></div>
</div>
```

## メリットとデメリット

### メリット

- **豊富なコンポーネント**: すぐに使えるUIコンポーネント
- **レスポンシブ対応**: モバイル対応が簡単
- **統一感**: 一貫性のあるデザイン
- **ドキュメント充実**: 学習リソースが豊富

### デメリット

- **ファイルサイズ**: CSSフレームワークの読み込みで重くなる
- **スタイル競合**: Marpのデフォルトスタイルと競合する可能性
- **カスタマイズ制限**: テーマとの調整が必要
- **オフライン制限**: CDNに依存するとオフラインで使えない

## 推奨事項

### Tailwind CSSが適している場合

- 細かいカスタマイズが必要
- ユーティリティクラスを好む
- モダンなデザインが必要

### Bootstrapが適している場合

- 既存のBootstrapプロジェクトとの統合
- コンポーネント重視
- 素早くプロトタイプを作成

### カスタムCSSが適している場合

- 軽量性を重視
- オフライン環境での使用
- 完全なコントロールが必要
- 既存のMarpテーマとの完全な互換性

## セキュリティ注意事項

HTMLタグやscriptタグを有効にする場合は、以下の設定が必要です：

```json
{
  "markdown.marp.enableHtml": true
}
```

ただし、これはセキュリティリスクを伴うため、信頼できるコンテンツのみで使用してください。

## まとめ

CSSフレームワークの統合は可能ですが、Marpの設計思想（KISS原則）を考慮すると、シンプルなカスタムCSSの方が適している場合が多いです。プロジェクトの要件に応じて選択してください。

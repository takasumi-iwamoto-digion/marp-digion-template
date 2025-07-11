# レイアウト手法の比較

Marpでレイアウトを構築する3つの手法を比較します。

## 1. カスタムCSSクラス（現在の実装）

### 実装例

```css
.columns {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 2rem;
}
```

### メリット

- ✅ **軽量**: 必要最小限のCSSのみ
- ✅ **高速**: 外部リソース不要
- ✅ **オフライン対応**: 完全にローカルで動作
- ✅ **カスタマイズ性**: 完全なコントロール
- ✅ **Marp最適化**: テーマとの完全な互換性

### デメリット

- ❌ 実装の手間
- ❌ 限定的な機能
- ❌ メンテナンスコスト

## 2. Tailwind CSS

### 実装例

```html
<div class="grid grid-cols-2 gap-4">
  <div class="bg-gray-100 p-4 rounded">...</div>
</div>
```

### メリット

- ✅ **豊富なユーティリティ**: 数千のクラス
- ✅ **一貫性**: デザインシステム
- ✅ **開発速度**: 素早いプロトタイピング
- ✅ **レスポンシブ**: モバイル対応が簡単

### デメリット

- ❌ **ファイルサイズ**: CDN読み込み（~40KB）
- ❌ **学習曲線**: クラス名の習得
- ❌ **HTMLの肥大化**: クラス名が長い
- ❌ **オンライン依存**: CDN必須

## 3. Bootstrap

### 実装例

```html
<div class="row">
  <div class="col-md-6">...</div>
</div>
```

### メリット

- ✅ **成熟度**: 長年の実績
- ✅ **コンポーネント**: 豊富な既製品
- ✅ **ドキュメント**: 充実した資料
- ✅ **互換性**: 広いブラウザサポート

### デメリット

- ❌ **重い**: 大きなファイルサイズ（~60KB）
- ❌ **画一的**: デザインが似通う
- ❌ **カスタマイズ困難**: 独自デザインが難しい
- ❌ **jQuery依存**: 一部機能で必要

## パフォーマンス比較

| 項目             | カスタムCSS | Tailwind | Bootstrap |
| ---------------- | ----------- | -------- | --------- |
| 初期読み込み時間 | ⭐⭐⭐⭐⭐  | ⭐⭐⭐   | ⭐⭐      |
| ファイルサイズ   | ~5KB        | ~40KB    | ~60KB     |
| レンダリング速度 | ⭐⭐⭐⭐⭐  | ⭐⭐⭐⭐ | ⭐⭐⭐    |
| メモリ使用量     | 最小        | 中       | 大        |

## 使用シーン別推奨

### カスタムCSSを選ぶべき場合

- 🎯 社内プレゼンテーション
- 🎯 オフライン環境での使用
- 🎯 パフォーマンス重視
- 🎯 ブランドデザインの厳密な適用

### Tailwind CSSを選ぶべき場合

- 🎯 プロトタイプ作成
- 🎯 モダンなUI要求
- 🎯 開発速度重視
- 🎯 複雑なレイアウト

### Bootstrapを選ぶべき場合

- 🎯 既存Bootstrapプロジェクト
- 🎯 標準的なUIで十分
- 🎯 学習コスト最小化
- 🎯 レガシーブラウザ対応

## 実装の複雑さ

### 2カラムレイアウトの比較

**カスタムCSS**

```html
<div class="columns">
  <div>左</div>
  <div>右</div>
</div>
```

行数: 4行

**Tailwind CSS**

```html
<div class="grid grid-cols-2 gap-4 p-4">
  <div class="bg-gray-100 p-4 rounded shadow">左</div>
  <div class="bg-gray-100 p-4 rounded shadow">右</div>
</div>
```

行数: 4行（ただしクラスが長い）

**Bootstrap**

```html
<div class="container-fluid">
  <div class="row g-3">
    <div class="col-md-6">
      <div class="card">
        <div class="card-body">左</div>
      </div>
    </div>
    <div class="col-md-6">
      <div class="card">
        <div class="card-body">右</div>
      </div>
    </div>
  </div>
</div>
```

行数: 15行

## 結論

**Marpでのプレゼンテーション作成には、カスタムCSSが最適です。**

理由：

1. **Marpの設計思想に合致** - シンプルで軽量
2. **最高のパフォーマンス** - 読み込みが高速
3. **完全なオフライン対応** - 環境を選ばない
4. **保守性** - 依存関係なし

ただし、以下の場合はフレームワークも検討価値があります：

- 短期間でのプロトタイプ作成
- 既存プロジェクトとの統合
- 高度なインタラクティブ要素が必要

最終的には、プロジェクトの要件と制約に基づいて選択することが重要です。

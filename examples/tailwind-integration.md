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

<!-- _class: title -->
<!-- _paginate: false -->

# Tailwind CSS統合デモ

CSSフレームワークでより柔軟なレイアウトを実現

<div class="date">2025年1月15日</div>
<div class="info">資料種別：技術デモ</div>
<div class="version">Ver.1.0</div>
<div class="company">株式会社DigiOn</div>

---

## Tailwindグリッドシステム

<div class="grid grid-cols-3 gap-4">
  <div class="bg-red-50 p-4 rounded-lg border border-red-200">
    <h3 class="text-red-600 font-bold mb-2">高速処理</h3>
    <p class="text-sm text-gray-700">新アルゴリズムによる3倍速</p>
  </div>
  <div class="bg-blue-50 p-4 rounded-lg border border-blue-200">
    <h3 class="text-blue-600 font-bold mb-2">安定性</h3>
    <p class="text-sm text-gray-700">99.9%の稼働率を実現</p>
  </div>
  <div class="bg-green-50 p-4 rounded-lg border border-green-200">
    <h3 class="text-green-600 font-bold mb-2">拡張性</h3>
    <p class="text-sm text-gray-700">プラグインで機能追加可能</p>
  </div>
</div>

---

## Flexboxレイアウト

<div class="flex gap-6 items-center">
  <div class="flex-1">
    <div class="bg-gradient-to-r from-red-500 to-pink-500 text-white p-6 rounded-xl shadow-lg">
      <h3 class="text-2xl font-bold mb-2">売上高</h3>
      <p class="text-3xl font-bold">410億円</p>
      <p class="text-sm opacity-80">前年比 +23%</p>
    </div>
  </div>
  <div class="flex-1">
    <div class="bg-gradient-to-r from-blue-500 to-cyan-500 text-white p-6 rounded-xl shadow-lg">
      <h3 class="text-2xl font-bold mb-2">営業利益</h3>
      <p class="text-3xl font-bold">72億円</p>
      <p class="text-sm opacity-80">前年比 +35%</p>
    </div>
  </div>
</div>

---

## カードコンポーネント

<div class="grid grid-cols-2 gap-6">
  <div class="bg-white rounded-lg shadow-md overflow-hidden">
    <div class="bg-red-600 text-white p-4">
      <h3 class="text-xl font-bold">プロダクトA</h3>
    </div>
    <div class="p-4">
      <ul class="space-y-2">
        <li class="flex items-center">
          <span class="text-green-500 mr-2">✓</span>
          高速処理エンジン
        </li>
        <li class="flex items-center">
          <span class="text-green-500 mr-2">✓</span>
          AI自動最適化
        </li>
        <li class="flex items-center">
          <span class="text-green-500 mr-2">✓</span>
          24時間サポート
        </li>
      </ul>
    </div>
  </div>
  
  <div class="bg-white rounded-lg shadow-md overflow-hidden">
    <div class="bg-blue-600 text-white p-4">
      <h3 class="text-xl font-bold">プロダクトB</h3>
    </div>
    <div class="p-4">
      <ul class="space-y-2">
        <li class="flex items-center">
          <span class="text-green-500 mr-2">✓</span>
          直感的UI
        </li>
        <li class="flex items-center">
          <span class="text-green-500 mr-2">✓</span>
          マルチプラットフォーム
        </li>
        <li class="flex items-center">
          <span class="text-green-500 mr-2">✓</span>
          カスタマイズ可能
        </li>
      </ul>
    </div>
  </div>
</div>

---

## プログレスバー表示

<div class="space-y-4">
  <div>
    <div class="flex justify-between mb-1">
      <span class="text-sm font-medium">開発進捗</span>
      <span class="text-sm font-medium">75%</span>
    </div>
    <div class="w-full bg-gray-200 rounded-full h-2.5">
      <div class="bg-red-600 h-2.5 rounded-full" style="width: 75%"></div>
    </div>
  </div>
  
  <div>
    <div class="flex justify-between mb-1">
      <span class="text-sm font-medium">テスト完了率</span>
      <span class="text-sm font-medium">60%</span>
    </div>
    <div class="w-full bg-gray-200 rounded-full h-2.5">
      <div class="bg-blue-600 h-2.5 rounded-full" style="width: 60%"></div>
    </div>
  </div>
  
  <div>
    <div class="flex justify-between mb-1">
      <span class="text-sm font-medium">ドキュメント作成</span>
      <span class="text-sm font-medium">90%</span>
    </div>
    <div class="w-full bg-gray-200 rounded-full h-2.5">
      <div class="bg-green-600 h-2.5 rounded-full" style="width: 90%"></div>
    </div>
  </div>
</div>

---

## レスポンシブデザイン

<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
  <div class="bg-gray-100 p-4 text-center rounded">
    <div class="text-3xl font-bold text-red-600">156</div>
    <div class="text-sm text-gray-600">アクティブユーザー</div>
  </div>
  <div class="bg-gray-100 p-4 text-center rounded">
    <div class="text-3xl font-bold text-blue-600">98.5%</div>
    <div class="text-sm text-gray-600">満足度</div>
  </div>
  <div class="bg-gray-100 p-4 text-center rounded">
    <div class="text-3xl font-bold text-green-600">24/7</div>
    <div class="text-sm text-gray-600">サポート体制</div>
  </div>
  <div class="bg-gray-100 p-4 text-center rounded">
    <div class="text-3xl font-bold text-purple-600">50+</div>
    <div class="text-sm text-gray-600">連携サービス</div>
  </div>
</div>

---

<!-- _class: end -->
<!-- _paginate: false -->

<div class="company-info">
  <div class="col1"></div>
  <div class="col2"></div>
  <div class="col3"></div>
  <div class="col4"></div>
  <div class="col5"></div>
</div>

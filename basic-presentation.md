---
marp: true
theme: digion
transition: fade
paginate: true
html: true
---

<!-- _class: title -->
<!-- _paginate: false -->


# DigiOn プレゼンテーション
基本から高度なレイアウトまで対応したMarpテンプレート

<div class="date">2025年1月15日</div>
<div class="info">資料種別：デモ資料</div>
<div class="version">Ver.1.0</div>
<div class="company">株式会社DigiOn</div>

---

## DigiOnテーマの特徴

プロフェッショナルなプレゼンテーションを簡単に作成：

- **豊富なレイアウト**: タイトル、通常、見出し、画像配置など多彩なスライドタイプ
- **統一されたデザイン**: DigiOnブランドカラーとフォントで一貫性のある見た目
- **簡単な使い方**: `theme: digion` を指定するだけですぐに利用可能
- **柔軟なカスタマイズ**: コードブロック、テーブル、グラフなど様々なコンテンツに対応

---

## 本日のアジェンダ

<div class="columns">
<div>

### 1. データビジュアライゼーション
- 月間アクティブユーザー数推移
- 売上構成比の変化
- 四半期業績サマリー
- ユーザー満足度調査
- 市場シェア分析

</div>
<div>

### 2. 基本レイアウト
- 通常スライド
- 画像配置レイアウト

### 3. コンテンツ表示機能
- フラグメント機能
- コードブロック
- テーブル

### 4. 高度なレイアウト
- カラムレイアウト各種

### 5. フレームワーク統合
- Bootstrap活用例

</div>
</div>

---

<!-- _class: headline -->
<!-- _paginate: false -->

## データビジュアライゼーション

---

## 月間アクティブユーザー数推移

<div class="columns">
<div>

- **前月比15%増加**
- 新機能リリースの効果が顕著
- 特に20-30代の利用が活発化
- 継続率も5ポイント改善

</div>
<div>

![width:350px](https://quickchart.io/chart?w=350&h=300&c={type:'bar',data:{labels:['7月','8月','9月','10月','11月','12月'],datasets:[{label:'アクティブユーザー数（万人）',data:[45,52,58,65,72,83],backgroundColor:'%23E60012',borderColor:'%23E60012',borderWidth:1}]},options:{responsive:true,maintainAspectRatio:false,scales:{y:{beginAtZero:true,grid:{color:'rgba(0,0,0,0.1)'}},x:{grid:{display:false}}},plugins:{legend:{display:false}}}})

</div>
</div>

---

## 売上構成比の変化

<div class="columns">
<div style="text-align: center;">

![width:220px](https://quickchart.io/chart?w=300&h=300&c={type:'pie',data:{labels:['プロダクトA','プロダクトB','プロダクトC'],datasets:[{data:[45,35,20],backgroundColor:['%23E60012','%23666666','%23999999']}]},options:{plugins:{legend:{display:false}}}})

### Q1

</div>
<div style="text-align: center;">

![width:220px](https://quickchart.io/chart?w=300&h=300&c={type:'pie',data:{labels:['プロダクトA','プロダクトB','プロダクトC'],datasets:[{data:[52,30,18],backgroundColor:['%23E60012','%23666666','%23999999']}]},options:{plugins:{legend:{display:false}}}})

### Q2

</div>
</div>

<div style="margin-top: 30px; text-align: center;">
  <span style="display: inline-block; margin: 0 20px;">
    <span style="display: inline-block; width: 20px; height: 20px; background: #E60012; vertical-align: middle;"></span>
    <strong>プロダクトA</strong>: 45% → 52% (+7pt)
  </span>
  <span style="display: inline-block; margin: 0 20px;">
    <span style="display: inline-block; width: 20px; height: 20px; background: #666666; vertical-align: middle;"></span>
    <strong>プロダクトB</strong>: 35% → 30% (-5pt)
  </span>
  <span style="display: inline-block; margin: 0 20px;">
    <span style="display: inline-block; width: 20px; height: 20px; background: #999999; vertical-align: middle;"></span>
    <strong>プロダクトC</strong>: 20% → 18% (-2pt)
  </span>
</div>

---

## 四半期業績サマリー

<div class="columns">
<div style="text-align: center;">

### 売上高（億円）
![width:280px](https://quickchart.io/chart?w=350&h=250&c={type:'line',data:{labels:['Q1','Q2','Q3','Q4'],datasets:[{label:'売上高',data:[320,350,385,410],borderColor:'%23E60012',backgroundColor:'rgba(230,0,18,0.1)',fill:true,tension:0.3}]},options:{plugins:{legend:{display:false}},scales:{y:{beginAtZero:false,min:300}}}})

前年同期比 **+23%**

</div>
<div style="text-align: center;">

### 営業利益（億円）
![width:280px](https://quickchart.io/chart?w=350&h=250&c={type:'line',data:{labels:['Q1','Q2','Q3','Q4'],datasets:[{label:'営業利益',data:[45,52,61,72],borderColor:'%23E60012',backgroundColor:'rgba(230,0,18,0.1)',fill:true,tension:0.3}]},options:{plugins:{legend:{display:false}},scales:{y:{beginAtZero:false,min:40}}}})

前年同期比 **+35%**

</div>
</div>

---

## ユーザー満足度調査結果

<div class="columns">
<div>

![width:100%](https://quickchart.io/chart?w=300&h=250&c={type:'doughnut',data:{labels:['非常に満足','満足','普通','不満','非常に不満'],datasets:[{data:[35,40,18,5,2],backgroundColor:['%23E60012','%23FF6666','%23CCCCCC','%23999999','%23666666']}]},options:{plugins:{legend:{position:'bottom',labels:{boxWidth:12,padding:10}}}}})

</div>
<div style="background-color: #f8f8f8; padding: 20px; border-radius: 8px;">

### 主な改善ポイント
- レスポンスタイムの改善
- 新機能のチュートリアル充実
- カスタマーサポート体制強化

<small style="color: #666;">※ n=1,234 / 調査期間: 2024年12月</small>

</div>
</div>

---

## 市場シェア分析

<div style="text-align: center;">

![width:550px](https://quickchart.io/chart?w=600&h=300&c={type:'line',data:{labels:['2022/Q1','2022/Q2','2022/Q3','2022/Q4','2023/Q1','2023/Q2','2023/Q3','2023/Q4','2024/Q1'],datasets:[{label:'当社',data:[22.3,23.1,24.2,25.0,25.8,26.5,27.2,27.9,28.5],borderColor:'%23E60012',borderWidth:3,tension:0.3},{label:'競合A',data:[26.5,26.2,25.8,25.5,25.2,24.9,24.6,24.4,24.2],borderColor:'%23666666',borderWidth:2,tension:0.3},{label:'競合B',data:[20.1,19.8,19.5,19.3,19.1,18.9,18.8,18.7,18.7],borderColor:'%23999999',borderWidth:2,tension:0.3}]},options:{scales:{y:{beginAtZero:false,min:15,max:30}},plugins:{legend:{display:false}}}})

</div>

<div class="columns-3" style="text-align: center; margin-top: 25px;">
<div>

<span style="display: inline-block; width: 30px; height: 4px; background-color: #E60012;"></span>  
当社: **28.5%**

</div>
<div>

<span style="display: inline-block; width: 30px; height: 4px; background-color: #666666;"></span>  
競合A: 24.2%

</div>
<div>

<span style="display: inline-block; width: 30px; height: 4px; background-color: #999999;"></span>  
競合B: 18.7%

</div>
</div>

---

<!-- _class: headline -->
<!-- _paginate: false -->

## 基本レイアウト

---

## 通常のスライド（default）

これは通常のスライドレイアウトです。`target/DigiOn-Template-default.png`のデザインを再現しています。

- 赤いアクセントカラーの見出し
- 標準的な箇条書きスタイル
- ページ番号の表示

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

<!-- _class: headline -->
<!-- _paginate: false -->

## コンテンツ表示機能

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

<!-- _class: headline -->
<!-- _paginate: false -->

## 高度なレイアウト

---

## 2カラムレイアウト（Grid）

<div class="columns">
<div>

### 左カラム
- Grid方式による2分割
- レスポンシブ対応
- 均等幅での表示

</div>
<div>

### 右カラム
- 画像やコードも配置可能
- 見やすいレイアウト
- コンテンツの整理に最適

</div>
</div>

---

## 3カラムレイアウト

<div class="columns-3">
<div>

### 製品A
- 高速処理
- 安定性重視
- 24時間稼働

</div>
<div>

### 製品B
- 使いやすさ
- 多機能
- カスタマイズ可能

</div>
<div>

### 製品C
- コストパフォーマンス
- 軽量設計
- モバイル対応

</div>
</div>

---

## 非対称レイアウト（40:60）

<div class="columns-40-60">
<div>

### 概要
当社の最新技術により、従来比3倍の処理速度を実現

</div>
<div>

### 詳細説明
- **処理速度**: 新アルゴリズムによる並列処理の最適化
- **メモリ効率**: スマートキャッシュシステムの導入
- **省電力**: AI駆動の電力管理システム
- **互換性**: 既存システムとの完全互換を維持

</div>
</div>

---

<!-- _class: headline -->
<!-- _paginate: false -->

## フレームワーク統合

---

## Bootstrap統合デモ

<div class="container-fluid p-0">
  <div class="row g-3">
    <div class="col-md-4">
      <div class="alert alert-success" role="alert">
        <h6 class="alert-heading mb-1">✓ 成功</h6>
        <small>目標達成率 150%</small>
      </div>
    </div>
    <div class="col-md-4">
      <div class="alert alert-info" role="alert">
        <h6 class="alert-heading mb-1">📊 情報</h6>
        <small>新機能リリース</small>
      </div>
    </div>
    <div class="col-md-4">
      <div class="alert alert-warning" role="alert">
        <h6 class="alert-heading mb-1">⚠️ 注意</h6>
        <small>メンテナンス予定</small>
      </div>
    </div>
  </div>
</div>

### ステータス表示

<div class="mt-3">
  <span class="badge bg-danger me-2">重要</span>
  <span class="badge bg-success me-2">完了</span>
  <span class="badge bg-primary me-2">進行中</span>
  <span class="badge bg-secondary">保留</span>
</div>

---

## Bootstrapテーブル

<table class="table table-striped table-hover">
  <thead class="table-dark">
    <tr>
      <th>プロジェクト</th>
      <th>進捗</th>
      <th>期限</th>
      <th>ステータス</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>新機能開発</td>
      <td>
        <div class="progress" style="height: 20px;">
          <div class="progress-bar bg-success" style="width: 75%">75%</div>
        </div>
      </td>
      <td>2025/02/28</td>
      <td><span class="badge bg-success">進行中</span></td>
    </tr>
    <tr>
      <td>バグ修正</td>
      <td>
        <div class="progress" style="height: 20px;">
          <div class="progress-bar bg-info" style="width: 90%">90%</div>
        </div>
      </td>
      <td>2025/01/31</td>
      <td><span class="badge bg-primary">レビュー中</span></td>
    </tr>
    <tr>
      <td>ドキュメント作成</td>
      <td>
        <div class="progress" style="height: 20px;">
          <div class="progress-bar bg-warning" style="width: 50%">50%</div>
        </div>
      </td>
      <td>2025/03/15</td>
      <td><span class="badge bg-warning text-dark">作業中</span></td>
    </tr>
  </tbody>
</table>

---

## Bootstrapカード＆リスト

<div class="row g-3">
  <div class="col-md-6">
    <div class="card border-danger">
      <div class="card-header bg-danger text-white">
        <h5 class="mb-0">重要タスク</h5>
      </div>
      <div class="card-body">
        <ul class="list-group list-group-flush">
          <li class="list-group-item d-flex justify-content-between align-items-center">
            セキュリティ更新
            <span class="badge bg-danger rounded-pill">3</span>
          </li>
          <li class="list-group-item d-flex justify-content-between align-items-center">
            パフォーマンス改善
            <span class="badge bg-warning rounded-pill">5</span>
          </li>
          <li class="list-group-item d-flex justify-content-between align-items-center">
            バグ修正
            <span class="badge bg-info rounded-pill">12</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
  <div class="col-md-6">
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">プロジェクト概要</h5>
        <p class="card-text">Bootstrap統合により、より洗練されたUIコンポーネントを簡単に実装できます。</p>
        <button class="btn btn-danger">詳細を見る</button>
        <button class="btn btn-outline-secondary">キャンセル</button>
      </div>
    </div>
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
---
marp: true
theme: digion
transition: fade
paginate: true
---

<!-- _class: title -->
<!-- _paginate: false -->


# DigiOn プレゼンテーション
シンプルな構成で使いやすいMarpテンプレート

<div class="date">2025年1月15日</div>
<div class="info">資料種別：デモ資料</div>
<div class="version">Ver.1.0</div>
<div class="company">株式会社DigiOn</div>

---

## テンプレートの特徴

このテンプレートは以下の改善を行いました：

- **シンプルなファイル構成**: ルートに必要なファイルを配置
  - test
    - test2
- **統一されたパス**: どの環境でも `./marp-custom-fixed.css`
- **画像の整理**: `images/` ディレクトリに集約
- **ドキュメント**: `docs/` ディレクトリに整理

---

## 月間アクティブユーザー数推移

<div style="display: flex; align-items: center; gap: 40px;">
  <div style="flex: 1;">
    <img src="https://quickchart.io/chart?c={type:'bar',data:{labels:['1月','2月','3月','4月','5月'],datasets:[{label:'ユーザー数',data:[12000,13500,15200,16800,19320],backgroundColor:'%23E60012'}]},options:{plugins:{legend:{display:false}},scales:{y:{beginAtZero:true}}}}" style="width: 100%;">
  </div>
  <div style="flex: 1;">
    <ul style="font-size: 20px;">
      <li><strong>前月比15%増加</strong></li>
      <li>新機能リリースの効果が顕著</li>
      <li>特に20-30代の利用が活発化</li>
      <li>継続率も5ポイント改善</li>
    </ul>
  </div>
</div>

---

## 売上構成比の変化

<div style="display: flex; flex-direction: column; gap: 20px;">
  <div style="text-align: center;">
    <div style="display: flex; justify-content: center; gap: 40px; margin: 20px 0;">
      <div>
        <img src="https://quickchart.io/chart?c={type:'doughnut',data:{labels:['プロダクトA','プロダクトB','プロダクトC'],datasets:[{data:[45,35,20],backgroundColor:['%23E60012','%23666666','%23999999']}]},options:{plugins:{title:{display:true,text:'2024 Q1'}}}}" style="width: 250px;">
      </div>
      <div>
        <img src="https://quickchart.io/chart?c={type:'doughnut',data:{labels:['プロダクトA','プロダクトB','プロダクトC'],datasets:[{data:[52,30,18],backgroundColor:['%23E60012','%23666666','%23999999']}]},options:{plugins:{title:{display:true,text:'2024 Q2'}}}}" style="width: 250px;">
      </div>
    </div>
  </div>
  <div style="display: flex; justify-content: space-around; font-size: 18px;">
    <div>
      <div style="display: inline-block; width: 15px; height: 15px; background: #E60012; margin-right: 5px;"></div>
      <strong>プロダクトA</strong><br>
      45% → 52% (+7pt)
    </div>
    <div>
      <div style="display: inline-block; width: 15px; height: 15px; background: #666; margin-right: 5px;"></div>
      <strong>プロダクトB</strong><br>
      35% → 30% (-5pt)
    </div>
    <div>
      <div style="display: inline-block; width: 15px; height: 15px; background: #999; margin-right: 5px;"></div>
      <strong>プロダクトC</strong><br>
      20% → 18% (-2pt)
    </div>
  </div>
</div>

---

## 四半期業績サマリー

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 30px;">
  <div>
    <h3 style="font-size: 24px; color: #E60012;">売上高（億円）</h3>
    <img src="https://quickchart.io/chart?c={type:'bar',data:{labels:['Q1','Q2','Q3','Q4'],datasets:[{label:'売上高',data:[120,140,165,180],backgroundColor:'%23E60012'}]},options:{plugins:{legend:{display:false}},scales:{y:{beginAtZero:true}}}}" style="width: 100%;">
    <p style="font-size: 16px; margin-top: 10px;">前年同期比 <strong>+23%</strong></p>
  </div>
  <div>
    <h3 style="font-size: 24px; color: #E60012;">営業利益（億円）</h3>
    <img src="https://quickchart.io/chart?c={type:'bar',data:{labels:['Q1','Q2','Q3','Q4'],datasets:[{label:'営業利益',data:[20,25,30,35],backgroundColor:'%23666666'}]},options:{plugins:{legend:{display:false}},scales:{y:{beginAtZero:true}}}}" style="width: 100%;">
    <p style="font-size: 16px; margin-top: 10px;">前年同期比 <strong>+35%</strong></p>
  </div>
</div>

---

## ユーザー満足度調査結果

<div style="display: flex; gap: 30px; align-items: flex-start;">
  <div style="flex: 1.5;">
    <img src="https://quickchart.io/chart?c={type:'horizontalBar',data:{labels:['UI/UX','機能の充実度','サポート対応','価格満足度','総合評価'],datasets:[{label:'スコア',data:[4.2,4.5,4.8,3.8,4.3],backgroundColor:['%23E60012','%23E60012','%23E60012','%23666666','%23E60012']}]},options:{plugins:{legend:{display:false}},scales:{x:{min:0,max:5}}}}" style="width: 100%;">
  </div>
  <div style="flex: 1; background-color: #f8f8f8; padding: 20px; border-radius: 8px;">
    <h3 style="font-size: 20px; margin-top: 0;">主な改善ポイント</h3>
    <ul style="font-size: 16px; line-height: 1.8;">
      <li>レスポンスタイムの改善</li>
      <li>新機能のチュートリアル充実</li>
      <li>カスタマーサポート体制強化</li>
    </ul>
    <p style="font-size: 14px; color: #666; margin-top: 15px;">
      ※ n=1,234 / 調査期間: 2024年12月
    </p>
  </div>
</div>

---

## 市場シェア分析

<div style="text-align: center;">
  <img src="https://quickchart.io/chart?c={type:'line',data:{labels:['2020','2021','2022','2023','2024'],datasets:[{label:'当社',data:[15,18,22,25,28.5],borderColor:'%23E60012',backgroundColor:'transparent',borderWidth:3},{label:'競合A',data:[13,13.5,14.5,20,24.2],borderColor:'%23666666',backgroundColor:'transparent',borderWidth:3},{label:'競合B',data:[10,10.5,11,15,18.7],borderColor:'%23999999',backgroundColor:'transparent',borderWidth:3}]},options:{scales:{y:{beginAtZero:true,max:30}}}}" style="width: 90%; max-width: 800px;">
  
  <div style="display: flex; justify-content: center; gap: 40px; font-size: 18px; margin-top: 20px;">
    <div style="display: flex; align-items: center; gap: 10px;">
      <div style="width: 20px; height: 3px; background-color: #E60012;"></div>
      <span>当社: <strong>28.5%</strong></span>
    </div>
    <div style="display: flex; align-items: center; gap: 10px;">
      <div style="width: 20px; height: 3px; background-color: #666;"></div>
      <span>競合A: 24.2%</span>
    </div>
    <div style="display: flex; align-items: center; gap: 10px;">
      <div style="width: 20px; height: 3px; background-color: #999;"></div>
      <span>競合B: 18.7%</span>
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
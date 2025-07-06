# QuickChart.io によるグラフ生成ガイド

このテンプレートでは、QuickChart.ioを使用して動的にグラフを生成しています。

## QuickChart.ioとは

QuickChart.ioは、URLパラメータでChart.jsの設定を渡すことで、動的にグラフ画像を生成するWebサービスです。

## 基本的な使い方

```markdown
![](https://quickchart.io/chart?c={chart_config})
```

`{chart_config}`の部分にChart.js形式の設定をJSON形式で記述します。

## 重要な注意点

- カラーコードの`#`は`%23`にURLエンコードする必要があります
- 日本語はそのまま使用できます
- スペースや特殊文字は適切にエンコードしてください

## グラフタイプ別の例

### 棒グラフ（Bar Chart）

```markdown
![](https://quickchart.io/chart?c={type:'bar',data:{labels:['7月','8月','9月'],datasets:[{label:'売上',data:[100,150,200],backgroundColor:'%23E60012'}]}})
```

### 円グラフ（Pie Chart）

```markdown
![](https://quickchart.io/chart?c={type:'pie',data:{labels:['A','B','C'],datasets:[{data:[30,40,30],backgroundColor:['%23E60012','%23666666','%23999999']}]}})
```

### 折れ線グラフ（Line Chart）

```markdown
![](https://quickchart.io/chart?c={type:'line',data:{labels:['Q1','Q2','Q3','Q4'],datasets:[{label:'売上',data:[100,120,140,160],borderColor:'%23E60012',tension:0.3}]}})
```

### ドーナツグラフ（Doughnut Chart）

```markdown
![](https://quickchart.io/chart?c={type:'doughnut',data:{labels:['満足','普通','不満'],datasets:[{data:[70,20,10],backgroundColor:['%23E60012','%23CCCCCC','%23666666']}]}})
```

## オプション設定

### 凡例の非表示

```javascript
options: {
  plugins: {
    legend: {
      display: false
    }
  }
}
```

### Y軸の最小値設定

```javascript
options:{scales:{y:{beginAtZero:false,min:100}}}
```

### グリッドラインの設定

```javascript
options:{scales:{y:{grid:{color:'rgba(0,0,0,0.1)'}},x:{grid:{display:false}}}}
```

## サイズ調整

Marpでは画像のサイズを以下のように調整できます：

```markdown
![width:400px](https://quickchart.io/chart?c=...)
![height:300px](https://quickchart.io/chart?c=...)
```

## トラブルシューティング

### グラフが表示されない場合

1. URLが正しくエンコードされているか確認
2. JSON構文が正しいか確認（特にクォートの位置）
3. QuickChart.ioのサイトで直接URLを試してみる

### 日本語が文字化けする場合

- UTF-8エンコードで日本語をそのまま使用できます
- 必要に応じてURLエンコードを使用してください

## 高度な使い方

### 複数データセット

```javascript
datasets: [
  { label: '当社', data: [10, 20, 30], borderColor: '%23E60012' },
  { label: '競合A', data: [15, 18, 22], borderColor: '%23666666' },
]
```

### カスタムフォント

QuickChart.ioはGoogle Fontsをサポートしていますが、日本語フォントは制限があります。

## 参考リンク

- [QuickChart.io公式サイト](https://quickchart.io/)
- [Chart.js公式ドキュメント](https://www.chartjs.org/docs/latest/)

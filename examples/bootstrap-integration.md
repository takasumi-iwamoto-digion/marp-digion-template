---
marp: true
theme: digion
style: |
  @import url('https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css');
  /* Bootstrapとの競合を調整 */
  section h1, section h2, section h3 {
    margin-top: 0 !important;
  }
  section .container-fluid {
    padding: 0;
  }
---

<!-- _class: title -->
<!-- _paginate: false -->

# Bootstrap統合デモ
定番CSSフレームワークでプロフェッショナルなレイアウト

<div class="date">2025年1月15日</div>
<div class="info">資料種別：技術デモ</div>
<div class="version">Ver.1.0</div>
<div class="company">株式会社DigiOn</div>

---

## Bootstrapグリッドシステム

<div class="container-fluid">
  <div class="row g-3">
    <div class="col-md-4">
      <div class="card border-danger">
        <div class="card-header bg-danger text-white">
          <h5 class="mb-0">機能A</h5>
        </div>
        <div class="card-body">
          <p class="card-text">高速データ処理エンジンを搭載</p>
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class="card border-primary">
        <div class="card-header bg-primary text-white">
          <h5 class="mb-0">機能B</h5>
        </div>
        <div class="card-body">
          <p class="card-text">リアルタイム同期機能</p>
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class="card border-success">
        <div class="card-header bg-success text-white">
          <h5 class="mb-0">機能C</h5>
        </div>
        <div class="card-body">
          <p class="card-text">AIによる自動最適化</p>
        </div>
      </div>
    </div>
  </div>
</div>

---

## アラートとバッジ

<div class="alert alert-success" role="alert">
  <h4 class="alert-heading">✓ 導入成功事例</h4>
  <p>大手企業100社以上での導入実績があります。</p>
</div>

<div class="alert alert-info" role="alert">
  <strong>情報:</strong> 新バージョン3.0がリリースされました
</div>

### ステータス表示

<h4>
  プロジェクト進捗 
  <span class="badge bg-danger">75%</span>
</h4>

<h4>
  品質スコア 
  <span class="badge bg-success">優秀</span>
</h4>

---

## リストグループとプログレスバー

<div class="row">
  <div class="col-md-6">
    <h4>タスクリスト</h4>
    <ul class="list-group">
      <li class="list-group-item">
        <input class="form-check-input me-2" type="checkbox" checked>
        要件定義完了
      </li>
      <li class="list-group-item">
        <input class="form-check-input me-2" type="checkbox" checked>
        設計書作成
      </li>
      <li class="list-group-item">
        <input class="form-check-input me-2" type="checkbox">
        実装中
      </li>
    </ul>
  </div>
  <div class="col-md-6">
    <h4>進捗状況</h4>
    <div class="mb-3">
      <label>開発: 75%</label>
      <div class="progress">
        <div class="progress-bar bg-danger" style="width: 75%"></div>
      </div>
    </div>
    <div class="mb-3">
      <label>テスト: 50%</label>
      <div class="progress">
        <div class="progress-bar bg-warning" style="width: 50%"></div>
      </div>
    </div>
  </div>
</div>

---

## テーブルスタイル

<table class="table table-striped table-hover">
  <thead class="table-dark">
    <tr>
      <th>製品名</th>
      <th>価格</th>
      <th>在庫</th>
      <th>状態</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>DigiOn Pro</td>
      <td>¥50,000</td>
      <td>150</td>
      <td><span class="badge bg-success">販売中</span></td>
    </tr>
    <tr>
      <td>DigiOn Standard</td>
      <td>¥30,000</td>
      <td>300</td>
      <td><span class="badge bg-success">販売中</span></td>
    </tr>
    <tr>
      <td>DigiOn Lite</td>
      <td>¥10,000</td>
      <td>0</td>
      <td><span class="badge bg-danger">在庫切れ</span></td>
    </tr>
  </tbody>
</table>

---

## ボタンとフォーム

<div class="row">
  <div class="col-md-6">
    <h4>アクションボタン</h4>
    <div class="d-grid gap-2">
      <button class="btn btn-danger btn-lg">購入する</button>
      <button class="btn btn-outline-primary">詳細を見る</button>
      <button class="btn btn-secondary">キャンセル</button>
    </div>
  </div>
  <div class="col-md-6">
    <h4>お問い合わせ</h4>
    <form>
      <div class="mb-2">
        <input type="email" class="form-control" placeholder="メールアドレス">
      </div>
      <div class="mb-2">
        <select class="form-select">
          <option>お問い合わせ種別を選択</option>
          <option>製品について</option>
          <option>サポート</option>
        </select>
      </div>
      <button type="submit" class="btn btn-primary w-100">送信</button>
    </form>
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
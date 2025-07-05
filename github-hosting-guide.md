# GitHub経由でのテーマ参照ガイド

## 概要

Marpのカスタムテーマと画像をGitHub経由で参照することで、ローカルファイルのコピーなしに共有・利用が可能になります。

## メリット

1. **一元管理**: テーマの更新が全ユーザーに自動反映
2. **簡単な共有**: URLを共有するだけで利用可能
3. **バージョン管理**: GitHubのバージョン管理機能を活用

## 実装方法

### 方法1: Markdownファイル内での直接指定

```yaml
---
marp: true
style: |
  @import url('https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fixed.css');
---
```

### 方法2: Marp CLIコマンドラインでの指定

```bash
# 単一ファイルの変換
marp --theme https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fixed.css slide.md

# 複数テーマの登録
marp --theme-set \
  https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fixed.css \
  https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fullhd.css \
  slide.md
```

### 方法3: 設定ファイル（.marprc.yml）での指定

```yaml
themeSet:
  - https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fixed.css
  - https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fullhd.css
```

### 方法4: package.jsonでの設定

```json
{
  "marp": {
    "themeSet": [
      "https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fixed.css",
      "https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/main/assets/marp-custom-fullhd.css"
    ]
  }
}
```

## 注意事項

### 1. URLの形式
- 必ず`raw.githubusercontent.com`を使用
- 通常のGitHub URLではなく、Raw URLを使用する必要があります

```
❌ https://github.com/user/repo/blob/main/file.css
✅ https://raw.githubusercontent.com/user/repo/main/file.css
```

### 2. プライベートリポジトリの場合

プライベートリポジトリの場合は、以下の方法でアクセス可能：

- **Personal Access Token**を使用
- GitHub ActionsのSecretsに保存して利用

```bash
# トークンを含むURL（非推奨）
https://raw.githubusercontent.com/user/repo/main/file.css?token=YOUR_TOKEN
```

### 3. キャッシュの問題

GitHubのCDNはファイルをキャッシュするため、更新が即座に反映されない場合があります：

- 最大5分程度の遅延が発生する可能性
- 強制的に最新版を取得するには、コミットハッシュを使用

```yaml
# ブランチ名の代わりにコミットハッシュを使用
@import url('https://raw.githubusercontent.com/user/repo/abc123def/assets/theme.css');
```

### 4. オフライン環境での制限

- インターネット接続が必要
- オフラインでのプレゼンテーションには不向き
- 重要な発表では事前にローカルコピーを用意

## 推奨される運用方法

### 開発環境
- ローカルファイルを使用して開発
- テスト後にGitHubへプッシュ

### 本番環境
- 安定版のタグやリリースを作成
- タグを指定してテーマを参照

```yaml
# タグを使用した安定版の参照
@import url('https://raw.githubusercontent.com/takasumi-iwamoto-digion/marp-digion-template/v1.0.0/assets/marp-custom-fixed.css');
```

### チーム共有
1. 中央リポジトリでテーマを管理
2. READMEに使用方法を記載
3. 定期的なバージョンアップとアナウンス

## トラブルシューティング

### テーマが読み込まれない場合

1. **URLの確認**: Raw URLを使用しているか
2. **ネットワーク**: プロキシやファイアウォールの設定
3. **リポジトリの公開設定**: プライベートの場合はアクセス権限
4. **CORSエラー**: ブラウザのセキュリティ設定

### 画像が表示されない場合

1. **画像URL**: CSS内の画像URLもGitHub経由になっているか確認
2. **ファイル名**: 大文字小文字の違いに注意（GitHubは大文字小文字を区別）
3. **拡張子**: 正しい拡張子を使用（.png/.jpg）
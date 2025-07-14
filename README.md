# apaiser - カジュアルフレンチレストラン

「apaiser（アペゼ）」は、"癒す・落ち着かせる"というフランス語の意味を名前に込めた、気取らず楽しめるカジュアルフレンチのお店のウェブサイトです。

## 技術スタック

### フロントエンド
- Vue 3 + TypeScript
- Vite (ビルドツール)
- Tailwind CSS (スタイリング)
- Vue Router (ルーティング)

### バックエンド
- NestJS + TypeScript
- PostgreSQL (データベース)
- TypeORM (ORM)

## セットアップ手順

### 前提条件
- Node.js (v18以上)
- npm または yarn
- PostgreSQL (v13以上)

### 1. リポジトリのクローン
```bash
git clone https://github.com/d-yamaguchi-surge/hp002.git
cd hp002
```

### 2. 依存関係のインストール
```bash
# ルートディレクトリで実行（全ての依存関係をインストール）
npm run install:all
```

### 3. データベースのセットアップ
PostgreSQLサーバーを起動し、データベースを作成してください：
```sql
CREATE DATABASE apaiser_db;
```

### 4. 環境変数の設定
```bash
# バックエンドの環境変数
cp backend/.env.example backend/.env
# 必要に応じてデータベース接続情報を編集

# フロントエンドの環境変数
cp frontend/.env.example frontend/.env
```

### 5. 開発サーバーの起動

#### 両方のサーバーを同時に起動（推奨）
```bash
npm run dev
```

#### 個別に起動する場合
```bash
# フロントエンド（ポート3000）
npm run dev:frontend

# バックエンド（ポート8000）
npm run dev:backend
```

## アクセス方法

- **フロントエンド**: http://localhost:3000
- **バックエンドAPI**: http://localhost:8000
- **ヘルスチェック**: http://localhost:8000/health

## プロジェクト構造

```
hp002/
├── frontend/          # Vue 3 + TypeScript フロントエンド
│   ├── src/
│   │   ├── components/    # Vueコンポーネント
│   │   ├── views/         # ページコンポーネント
│   │   ├── router/        # ルーティング設定
│   │   └── main.ts        # エントリーポイント
│   ├── index.html
│   ├── vite.config.ts
│   └── package.json
├── backend/           # NestJS + TypeScript バックエンド
│   ├── src/
│   │   ├── app.module.ts  # メインモジュール
│   │   ├── app.controller.ts
│   │   ├── app.service.ts
│   │   └── main.ts        # エントリーポイント
│   └── package.json
├── package.json       # ルートパッケージ（ワークスペース設定）
└── README.md
```

## 利用可能なスクリプト

- `npm run dev` - フロントエンドとバックエンドを同時に起動
- `npm run dev:frontend` - フロントエンドのみ起動
- `npm run dev:backend` - バックエンドのみ起動
- `npm run build` - 両方をビルド
- `npm run build:frontend` - フロントエンドをビルド
- `npm run build:backend` - バックエンドをビルド

## トラブルシューティング

### ポートが既に使用されている場合
- フロントエンド（3000番ポート）またはバックエンド（8000番ポート）が既に使用されている場合は、該当するプロセスを終了してから再度起動してください。

### データベース接続エラー
- PostgreSQLサーバーが起動していることを確認してください
- `backend/.env` ファイルのデータベース接続情報が正しいことを確認してください

### 依存関係のインストールエラー
- Node.jsのバージョンが18以上であることを確認してください
- `node_modules` フォルダを削除して再度 `npm run install:all` を実行してください

## 開発について

このプロジェクトはモバイルファーストのレスポンシブデザインを採用しており、ブランドカラーは `#258c6d` を使用しています。

フロントエンドの開発では、Tailwind CSSを使用してスタイリングを行い、Vue 3のComposition APIを活用しています。

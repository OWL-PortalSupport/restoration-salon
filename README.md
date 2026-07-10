# Restoration Salon

Restoration Salon は、UI/UX を重視した整体・リラクゼーションサロン向けサンプルサイトです。  
Vue 3 / Vite / TypeScript / Tailwind CSS を使用し、静的サイトとして公開できる構成で制作しています。

公開 URL: [https://owl-portalsupport.github.io/restoration-salon/](https://owl-portalsupport.github.io/restoration-salon/)

## 使用技術

- Vue 3
- TypeScript
- Vite
- Tailwind CSS
- Bun
- Docker

## 推奨環境

本プロジェクトでは、以下の環境を推奨します。

- Node.js: 20.19 以上、または 22.12 以上
- Bun: 最新の安定版を推奨
- Docker: Docker Desktop を推奨

Vite の動作要件に合わせるため、Node.js は 20.19 以上、または 22.12 以上を使用してください。  
Node.js 18 系は、現在の Vite 環境では非推奨です。

## セットアップ

依存パッケージをインストールします。

```sh
bun install
```

## 開発サーバーの起動

ローカル開発環境を起動します。

```sh
bun dev
```

起動後、ターミナルに表示されたローカル URL へアクセスして画面を確認します。

## 本番用ビルド

本番公開用のファイルを生成します。

```sh
bun run build
```

## Lint 実行

コードの静的チェックを実行します。

```sh
bun lint
```

## Docker の起動方法

Docker コンテナをバックグラウンドで起動します。

```sh
docker compose up -d
```

起動中のコンテナを確認します。

```sh
docker compose ps
```

ログを確認します。

```sh
docker compose logs -f
```

コンテナを停止します。

```sh
docker compose down
```

不要な古いコンテナが残っている場合は、以下のコマンドで削除しながら起動します。

```sh
docker compose up -d --remove-orphans
```

## Bun の基本コマンド

Bun のバージョンを確認します。

```sh
bun --version
```

依存パッケージをインストールします。

```sh
bun install
```

開発サーバーを起動します。

```sh
bun dev
```

本番用にビルドします。

```sh
bun run build
```

Lint を実行します。

```sh
bun lint
```

## 変更仕様

- Vite 初期テンプレートの README 内容を削除し、本プロジェクト用の説明に変更
- プロジェクト概要を Restoration Salon 向けに変更
- 使用技術に Vue 3 / TypeScript / Vite / Tailwind CSS / Bun / Docker を記載
- Node.js の必要バージョンを明記
- Bun を使用したセットアップ・開発・ビルド・Lint コマンドを追加
- Docker の起動、状態確認、ログ確認、停止方法を追加
- 古いコンテナが残っている場合の `--remove-orphans` コマンドを追加

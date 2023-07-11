# ブラックジャック_ブラウザゲーム：WEB

## 目的

* PHPとMySQLを使って、ブラックジャックゲームをブラウザでゲームできるようにする
* Webアプリケーションの仕組みの理解を深める->MVCモデルを使う。
* Dockerfileなどのベースは、学習サービスのを使用。自分で作成したわけではない。
* 「PHPを使って、MVCモデルを使いながら実装し、仕組みを理解する」のが趣旨である。

## 環境構築

```bash
# Docker イメージのビルド
docker-compose build

# Docker コンテナの起動
docker-compose up -d

# Docker コンテナ内でコマンドを実行する
docker-compose exec app php -v

# Docker コンテナの停止・削除
docker-compose down
```

## 環境構築 (Remote Development編)

Docker イメージをビルドする。

```bash
docker-compose build
```

VSCode の Remote-Containers: Open Folder in Container からコンテナを開く。

コマンドは VSCode のターミナルから実行する。

終了するときはコンテナを停止・削除する。

```bash
docker-compose down
```

## 静的解析

VSCode のターミナル上で下記コマンドを実行する（Remote Development で開発している場合）。

```bash
# PHPStan でコードのバグを検知する
composer phpstan

# PHP_CodeSniffer でコーディング規約に準拠していないコードを検知する
composer phpcs
```

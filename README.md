# Go 開発環境（Docker）
このリポジトリは、Docker を用いた Go のローカル開発環境を提供します。Go のバージョンや依存関係に左右されず、どこでも同じ環境で動作させることができます。

## 📁 ディレクトリ構成

```
go-dev/
├── docker-compose.yml
├── Dockerfile
├── .dockerignore
├── .gitignore
└── src/
    └── main.go
```

## 🚀 初期セットアップ

この環境ではローカルに Go をインストールせずに、Docker コンテナ内で開発・実行できます。

## ▶️ 実行

以下のコマンドで Go プログラムをビルド＆実行します：

```bash
cd src
docker compose run --rm go-dev go run main.go
```

## 📦 ビルド（任意）

Go バイナリをビルドするには以下を実行します：

```bash
docker compose run --rm go-dev go build -o app main.go
```

その後、ビルドされたバイナリを実行できます：

```bash
./app
```

※ビルド結果はホスト環境側に保存されます（Docker の共有ボリュームにより）。

## ✅ 前提条件

- Docker
- Docker Compose

## 📝 ライセンス
このプロジェクトは MIT License のもとで公開されています。

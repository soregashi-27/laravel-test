# 環境構築

1. Docker Desktop

上記は必ずインストールした上で始めてください。

## Macにおける初期設定

1. Terminal.app を開きます
2. `git clone git@github.com:SuguruOoki/tests.git` で自分のPCにこのリポジトリをダウンロードします
3. `cd tests` でカレントディレクトリをダウンロードしたディレクトリである `tests` に移動します。
4. `cp .env.example .env` を実行し、必要な環境の情報が書かれた `.env` ファイルを作成します。
5. `docker compose build --no-cache` を実行します。
6. ↓のような表示が流れていくことを確認してください

![d161a9cadf8e80bcaa66273d3f2ee10b](https://user-images.githubusercontent.com/16362021/149891105-ef42351e-006b-4985-95dc-a8c210ef19ea.gif)

7. `docker compose up -d` を実行します。
8. `docker compose ps` というコマンドを打って次のような表示になっていれば、環境構築は終了です。お疲れ様でした！

![スクリーンショット 2022-01-18 16 31 52](https://user-images.githubusercontent.com/16362021/149891200-e6da2ca6-662d-4cee-8ec6-816ef6c06b77.png)


## 画像の追加サイト
参考 \
https://picsum.photos/

## 使うコマンド
コンテナに入る

phpコンテナ
```
docker compose exec php bash
```

webコンテナ
```
docker compose exec nginx bash
```

DBコンテナ
```
docker compose exec mysql bash
```

webページへ接続
```
http://localhost:8888/
```

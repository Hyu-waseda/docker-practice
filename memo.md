## Dockerfile

Dockerfileからイメージを作成する
```shell
docker build .
docker build -t (作成したいイメージ名) .
```

イメージからコンテナを起動+コマンドを実行
```shell
docker run (REPOSITORY_NAMEまたはIMAGE_ID) CMD
docker run -it (REPOSITORY_NAMEまたはIMAGE_ID) CMD
docker run -d -p 8080:80(REPOSITORY_NAMEまたはIMAGE_ID) CMD
```
-d ... 抜けても起動継続

-p ... 自分のポート：仮想環境のポート

起動しているコンテナでコマンドを実行
```shell
docker exec CONTAINER_ID
docker exec -it CONTAINER_ID bash
```
-i ... interactive, 入力状態を維持する
-t ... tty, 疑似端末を割り当てる

起動しているコンテナを停止
```shell
docker stop CONTAINER_ID
```

コンテナを削除
```shell
docker rm CONTAINER_ID
```

イメージを削除
```shell
docker rmi (REPOSITORY_NAMEまたはIMAGE_ID)
```

## docker-compose
dockerを管理するツール
複雑なオプション、コンテナの連携など

Dockerfileからイメージを作成
```shell
docker-compose build
```

イメージからコンテナを起動+コマンドを実行
```shell
docker-compose run
```

起動しているコンテナでコマンドを実行
```shell
docker-compose exec
```

docker-compose.ymlに書いてあるコンテナを表示
```shell
docker-compose ps
```

コンテナを立ち上げる
```shell
docker-compose up
docker-compose up -d
```

コンテナを停止して削除
```shell
docker-compose down
```

## その他コマンド
イメージ一覧
```shell
docker image ls 
docker images
```

コンテナ一覧
```shell
docker container ls 
```
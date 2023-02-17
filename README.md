# imagemagick-test

ImageMagickインストール済みのUbuntuを起動します。  
`./resources`をマウントしてるので、コンテナに入って適当にコマンドを実行してください。  

```bash
# ビルド
docker compose build

# コンテナ起動
make up

# コンテナ接続
make exec
```
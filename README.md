# 開発環境
docker-composeサンプル
```yml
version: '3'
services:
  nuxt:
    build: nuxt-base
    restart: always
    volumes:
      - ./nuxt-base:/usr/src/app
```
初回起動時
```bash
docker-compose run --rm nuxt ash -c "yarn && yarn build"
```
リビルド&再起動
```bash
docker-compose exec nuxt yarn build && docker-compose restart nuxt
```
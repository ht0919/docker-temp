# Docker for Windows用のテンプレート

## 実行環境

- OS: Windows 10 Pro (1803)
- Docker for Windows: Version 18.06.0-ce-win72 (19098)

## 構築環境

- Ruby: 2.4.1
- Rails: 5.1.6
- MySQL: 5.7

## ファイル内容

- docker-compose.yml
- Dockerfile
- Gemfile
- Gemfile.lock (空)

## 操作手順

```
$ git clone https://github.com/ht0919/docker-temp.git
$ cd docker-temp
$ docker-compose run web rails new . --force --database=mysql
$ docker-compose build
※config/database.yml の host: localhost を host: db に修正
$ docker-compose up -d
$ docker-compose run web rake db:create
※ブラウザで http://localhost:3000/ を表示
```

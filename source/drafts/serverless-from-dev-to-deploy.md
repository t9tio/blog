---
title: 2019年开发和部署 serverless 单页应用最佳实践 (Chinese)
description: 记录了开发和部署 serverless 网站的最佳实践，这里所谓最佳实践，指的是最方便的方式
---

> 具体案例可以参考 [t9tio/cloudquery](https://github.com/t9tio/cloudquery)，本文是在更新该项目开发方式过后的一个总结

## 开发

### 目标：

- 一个命令启动整个开发环境 (docker-compose up)
- 前端：代码更新自动build，网页自动刷新
- 后端：代码更新服务器自动重启

### 配置：

docker-compose 组织前端后端数据库以便一键启动

```yml
version: "3"
services:
  # Undetermined: use node_modules inside docker or outside docker? it is a question https://stackoverflow.com/a/38601156/4674834
  backend:
    build:
      context: ./
      dockerfile: ./dockerfile
    image: backend_img
    ports:
      - "3000:3000"
    depends_on:
      - "dynamodb"
    working_dir: /code
    volumes:
      - .:/code
    command: sh -c "node /code/backend/db/initDb.js && nodemon /code/backend/index.js --ignore test/"

  frontend:
    image: backend_img
    ports:
      - "1234:1234"
    depends_on:
      - backend
    working_dir: /code
    volumes:
      - .:/code
    command: parcel /code/frontend/index.html
```

### 启动开发环境

```bash
docker-compose up
```

## 部署

目标：
一个命令自动部署前后端

方法：

up

例子：

up.json
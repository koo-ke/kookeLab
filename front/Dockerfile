# ベースイメージの指定
FROM node:19-alpine3.16

# ワークディレクトリの作成
RUN mkdir -p /front
WORKDIR /front

# ポート解放
EXPOSE 8080

# 利用可能パッケージのインデックスを更新
RUN apk update

# Nuxt3インストール
RUN npx nuxi init .

# Node.jpパッケージインストール
RUN npm install
RUN yarn install
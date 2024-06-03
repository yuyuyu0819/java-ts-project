# ベースイメージの指定
FROM node:16-alpine

# 作業ディレクトリの設定
WORKDIR /app

# アプリケーションの依存関係をインストール
COPY package.json ./
COPY package-lock.json ./
RUN npm install

# アプリケーションのソースコードをコピー
COPY . .

# アプリケーションのビルド
RUN npm run build

# サーバーを起動
CMD ["npm", "start"]

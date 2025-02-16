# 使用する Node.js のバージョンを指定
FROM node:16-alpine

# 作業ディレクトリを作成
WORKDIR /usr/src/app

# package.json と package-lock.json をコンテナにコピー
COPY package*.json ./

# 依存関係のインストール
RUN npm install

# アプリケーションのソースコードをコピー
COPY . ./

# アプリケーションのビルド
RUN npm run build

# サーバーを起動するコマンド（デフォルトは3000ポート）
CMD ["npm", "run", "start"]

# コンテナがリッスンするポートを指定
EXPOSE 3000

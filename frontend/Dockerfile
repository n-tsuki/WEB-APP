# ベースイメージを指定
FROM node:18

# アプリケーションディレクトリを作成
WORKDIR /app

# アプリケーションの依存関係をインストール
# package.json と package-lock.json をコピー
COPY package*.json ./
RUN npm install

# アプリケーションのソースをコピー
COPY . .

# アプリケーションをビルド
RUN npm run build

# アプリケーションを起動
CMD ["npm", "run", "dev"]

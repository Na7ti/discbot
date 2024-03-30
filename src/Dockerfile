# ベースイメージ
FROM node:20.11.1

# 作業ディレクトリ作成
WORKDIR /usr/src/discbot

# アプリケーションコードのコピー
COPY /src/ ./

# package.jsonの作成
# RUN npm init -y

# package.jsonに書いたパッケージをインストール
RUN npm install

# ExpressとDiscord.jsのインストール
RUN npm install -y \
    discord.js \
    dotenv

# ポートの公開 
EXPOSE 8000

# 起動時に実行するコマンド
CMD bash -c \
    "node command.js && \
    npm run dev"

FROM golang:1.19-alpine
# アップデートとgitのインストール
RUN apk update && apk add 

ENV CGO_ENABLED 0
# appディレクトリの作成
RUN mkdir /go/src/app
# ワーキングディレクトリの設定
WORKDIR /go/src/app
# ホストのファイルをコンテナの作業ディレクトリに移行
ADD ../.. /go/src/app
RUN go mod tidy
# コンテナ内で使用するポート
EXPOSE 8080



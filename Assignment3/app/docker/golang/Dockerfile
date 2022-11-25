# Specify the base image for the go app.
FROM golang:1.19

WORKDIR /go/src/github.com/postgres-go
# Copy everything from this project into the filesystem of the container.
COPY . .
# Obtain the package needed to run code. Alternatively use GO Modules. 
RUN go get -u github.com/lib/pq

# コンテナ作業ディレクトリの変更
WORKDIR /go/src/yuta/go
# ホストOSの ./go の中身を作業ディレクトリに追加
ADD ./go .
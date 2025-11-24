# Stage 1: Build
FROM golang:1.18 AS builder

WORKDIR /app

COPY main.go .

RUN go mod init guestbook
RUN go get -u github.com/gin-gonic/gin
RUN go mod tidy
RUN go build -o main main.go

# Stage 2: Final image
FROM ubuntu:18.04

COPY --from=builder /app/main /app/guestbook
COPY public/index.html /app/public/index.html
COPY public/script.js /app/public/script.js
COPY public/style.css /app/public/style.css
COPY public/jquery.min.js /app/public/jquery.min.js

WORKDIR /app

CMD ["./guestbook"]
EXPOSE 3000

FROM golang:1.26-alpine

RUN go install github.com/air-verse/air@latest

WORKDIR /app

COPY . .

WORKDIR /app/services/core-service

CMD ["air", "-c", ".air.toml"]
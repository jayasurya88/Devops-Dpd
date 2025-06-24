FROM golang:1.22-alpine
WORKDIR /app
COPY . .
RUN go build -o service1 main.go
RUN apk add --no-cache curl
EXPOSE 8001
CMD ["./service1"] 
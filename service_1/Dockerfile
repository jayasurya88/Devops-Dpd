FROM golang:1.22-alpine
WORKDIR /app
COPY . .
RUN go build -o service1 main.go
EXPOSE 5001
CMD ["./service1"] 
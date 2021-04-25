FROM golang:1.14.1-alpine as build
WORKDIR /app
ADD . .
RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -ldflags '-extldflags "-static"' -o main .
CMD ["go", "run", "main.go"]
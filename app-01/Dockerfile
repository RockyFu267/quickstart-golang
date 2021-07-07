FROM aslan-spock-register.qiniu.io/fuao/go:1.16 as build
WORKDIR /app
ADD . .
RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -ldflags '-extldflags "-static"' -o main .
CMD ["go", "run", "main.go"]

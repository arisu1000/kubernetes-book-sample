FROM golang:1.16 AS builder

WORKDIR /go/github.com/arisu1000/kubernetes-book-sample
COPY ./ ./
RUN go get && CGO_ENABLED=0 GOOS=linux go build -o sampleapp . 

# ENTRYPOINT [ "sampleapp" ]

FROM alpine:3.14

COPY --from=builder /go/github.com/arisu1000/kubernetes-book-sample/sampleapp /bin/sampleapp
ENTRYPOINT [ "sampleapp" ]
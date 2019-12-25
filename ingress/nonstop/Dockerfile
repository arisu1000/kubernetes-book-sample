FROM golang:1.12.10-stretch
WORKDIR /go/src/websample
COPY . .
RUN go install
ARG version
ENV version=${version}
CMD ["websample"]
FROM golang:alpine AS builder
RUN apk add git make
RUN go install github.com/jteeuwen/go-bindata/go-bindata@latest
WORKDIR /go/cowyo
RUN git clone https://github.com/schollz/cowyo.git .
RUN make build

FROM alpine:latest
VOLUME /data
EXPOSE 8050
COPY --from=builder /go/cowyo/cowyo /cowyo
ENTRYPOINT ["/cowyo"]
CMD ["--data","/data","--allow-file-uploads","--max-upload-mb","10","--host","0.0.0.0"]
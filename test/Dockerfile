FROM alpine:latest
RUN apk add --no-cache curl
RUN echo "Hello from $(uname -m)" > /arch.txt
CMD ["cat", "/arch.txt"]
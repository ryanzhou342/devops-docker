FROM golang:1.16

ENV PORT=8080
ENV REQUEST_ORIGIN=https://example.com

EXPOSE ${PORT}

WORKDIR /usr/src/app

COPY ./example-backend/ .

RUN go build

CMD ["./server"]
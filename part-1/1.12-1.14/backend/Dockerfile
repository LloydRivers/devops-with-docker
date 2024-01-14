FROM golang:1.16

WORKDIR /user/src/app

COPY . /user/src/app/

ENV REQUEST_ORIGIN=http://localhost:5000 PORT=8080

RUN go build

RUN go test ./...

CMD ["./server"]
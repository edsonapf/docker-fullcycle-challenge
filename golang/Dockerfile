FROM golang:1.24-alpine AS builder

WORKDIR /src

COPY main.go .

RUN go build main.go

FROM scratch

COPY --from=builder /src/main .

CMD ["/main"]
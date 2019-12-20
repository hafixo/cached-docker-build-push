FROM golang:1-alpine3.10 as builder

RUN apk add git
RUN go get github.com/urfave/cli

COPY src .

CMD ["go", "run", "main.go"]

FROM alpine3
COPY --from=builder build /build

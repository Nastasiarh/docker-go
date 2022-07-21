FROM golang:alpine as build
WORKDIR /go/bin
ADD . .
RUN CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build

FROM scratch
WORKDIR /go/bin
COPY --from=build /go/bin/docker-demo-2 /go/bin/docker-demo-2


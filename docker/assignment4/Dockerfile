FROM golang:alpine as builder
LABEL stage=builder
RUN apk add --update make
WORKDIR /apps
COPY go-app/ /apps  
RUN make build-linux

FROM alpine:latest
WORKDIR /apps
COPY --from=builder /apps/out /apps
CMD [ "./go-app" ]
FROM golang:alpine
RUN apk add --update make
WORKDIR /apps
COPY go-app/ /apps  
RUN make build-linux
CMD [ "./out/go-app" ]
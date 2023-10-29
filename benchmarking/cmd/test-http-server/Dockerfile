FROM golang:alpine

WORKDIR /app

COPY go.mod go.sum ./
RUN go mod download

COPY *.go ./

RUN go build -o /server

#EXPOSE 8080/tcp

ENTRYPOINT ["/server"]

#response size default to 512 KB initially
#CMD ["-port=8080", "-endpoint=/endpoint", "-response-size=512"]
# unnessasary if we already have the default values in code

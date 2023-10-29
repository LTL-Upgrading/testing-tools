FROM golang:alpine

WORKDIR /app

COPY go.mod go.sum ./
RUN go mod download

COPY *.go ./

RUN go build -o /client

ENTRYPOINT ["/client"]

#last para address should be the secondary network address in form of full URL with http head, of server we want to send  test request to
#CMD ["-requests=1", "-connect-timeout=1000", "-spinup-period=500", "-workers=1", "-startup-delay=0", "http://localhost:8080"]
# unnessasary if we already have the default values in code

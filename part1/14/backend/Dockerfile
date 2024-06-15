FROM golang:1.16
WORKDIR /usr/src/app
COPY go.mod go.sum ./
RUN go mod download && go mod verify
COPY . .
ENV PORT 8080
ENV REQUEST_ORIGIN=http://localhost:5000
RUN go test ./...
RUN go build
EXPOSE 8080
CMD ./server

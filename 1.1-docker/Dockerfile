FROM golang:1.11-alpine3.9 as builder
COPY ./main.go ./
RUN go build -o /main main.go

FROM scratch
EXPOSE 8080
COPY --from=builder /main ./
ENTRYPOINT ["./main"]

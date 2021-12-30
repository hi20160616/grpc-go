# gRPC-Gateway

```
protoc --go_out=. --go_opt=paths=source_relative \
    --go-grpc_out=. --go-grpc_opt=paths=source_relative \
    --grpc-gateway_out=. --grpc-gateway_opt=paths=source_relative \
    helloworld/helloworld.proto
```

Test grpc gateway
```
go run main.go // server
go run main.go // client for test
curl -X POST -k http://localhost:8080/v1/greeter/sayhello -d '{"name": "world"}'
```

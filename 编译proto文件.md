### Java版本编译
下载protoc-gen-grpc-java插件
https://repo1.maven.org/maven2/io/grpc/protoc-gen-grpc-java/1.25.0/
```
protoc --plugin=protoc-gen-grpc-java=build/exe/java_plugin/protoc-gen-grpc-java \
  --grpc-java_out="$OUTPUT_FILE" --proto_path="$DIR_OF_PROTO_FILE" "$PROTO_FILE"
  
protoc --plugin=protoc-gen-grpc-java=build/exe/java_plugin/protoc-gen-grpc-java \
  --grpc-java_out=lite:"$OUTPUT_FILE" --proto_path="$DIR_OF_PROTO_FILE" "$PROTO_FILE"
```
```
实例
protoc --plugin=protoc-gen-grpc-java=/Users/kunpeng/protoc-gen-grpc-java.exe --grpc-java_out=. --proto_path=. *.proto
```


### Golang版本编译

```
protoc --proto_path=$GOPATH/src:. --micro_out=. --go_out=. *.proto
```

```
https://github.com/grpc/grpc-java/blob/master/examples/src/main/proto/helloworld.proto
```

### Start Jaeger
```
$docker run -d --name jaeger \
  -e COLLECTOR_ZIPKIN_HTTP_PORT=9411 \
  -p 5775:5775/udp \
  -p 6831:6831/udp \
  -p 6832:6832/udp \
  -p 5778:5778 \
  -p 16686:16686 \
  -p 14268:14268 \
  -p 14250:14250 \
  -p 9411:9411 \
  jaegertracing/all-in-one:1.17
```

You can then navigate to http://localhost:16686 to access the Jaeger UI.

### Run
```
$go run hello.go
```


### Result
[img]
![alt text](https://raw.githubusercontent.com/up1/demo-go-opentelemetry/master/sample.png "Result")


Reference 
https://github.com/open-telemetry/opentelemetry-go/blob/master/sdk/trace/trace_test.go

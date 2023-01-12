
## check examples below

https://github.com/hyperium/tonic/blob/master/examples


### compression
```
use tonic::codec::CompressionEncoding;
```


server

```
let service = GreeterServer::new(greeter)
       .send_compressed(CompressionEncoding::Gzip)
       .accept_compressed(CompressionEncoding::Gzip);
```

client

```
let mut client = GreeterClient::new(channel)
        .send_compressed(CompressionEncoding::Gzip)
        .accept_compressed(CompressionEncoding::Gzip);
```
---

- tracing
- tower
- tls
- authentication
	with_interceptor(server, check_auth);
- interceptor
- ...



# Go

## HTTP

for most of basic usecases, the default `net/http` pkg will be all what u need. no need for searching around and trying any web frameworks for Golang.

### http server

- `gorilla/mux`
  - if u need more than `net/http`
  - https://github.com/gorilla/mux

### http client

- `resty`
  - wrapper of `net/http`
  - easy to set retrying options
  - https://github.com/go-resty/resty

## Testing

The default pkg, `testing` alr includes all features you need. Belows make things a bit easier, but there's no need to try to use them.

- `testify/assert`
  - a JUnit like pkg. easy to use.
  - https://github.com/stretchr/testify/

### mocking redis

- `miniredis`
  - https://github.com/alicebob/miniredis

### mocking http

- `httpmock`
  - https://github.com/jarcoal/httpmock

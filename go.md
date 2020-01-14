# Go

## HTTP

for most of basic usecases, the default `net/http` pkg will be all what u need. no need for searching around and try any web frameworks for Golang.

### http server

- gorilla mux
  - if u need more than `net/http`
  - https://github.com/gorilla/mux

### http client

- resty
  - wrapper of `net/http`
  - easy to set retrying options
  - https://github.com/go-resty/resty

## Testing

### mocking redis

- miniredis
  - https://github.com/alicebob/miniredis

### mocking http

- httpmock
  - https://github.com/jarcoal/httpmock

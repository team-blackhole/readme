# Go

## Syntax & Code Style

- init function; init()
  - init func is not highly recommended cos it makes global states.
  - what's this?: https://tutorialedge.net/golang/the-go-init-function/

- about interface and global state
  - https://peter.bourgon.org/blog/2017/06/09/theory-of-modern-go.html

- OOP
  - Is Go object-orientied?: https://flaviocopes.com/golang-is-go-object-oriented/

## CI

Gophers usually use Makefile to manage build processes.

- Makefile
  - https://kodfabrik.com/journal/a-good-makefile-for-go/?fbclid=IwAR25fSZWbT9Ij0OoJOlm8lAOGyUMN06Olmr79pgGzS9OWYNFG54TcGlG0c0

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

if u want to stop when got an error, use `t.Fatal(msg)`. If not, use `t.Error(msg)`.

- Table driven tests
  - let u manage many testcases easily
  - ref: https://dave.cheney.net/2019/05/07/prefer-table-driven-tests

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

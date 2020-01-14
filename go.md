<img src="https://www.vertica.com/wp-content/uploads/2019/07/Golang.png" width="400">

# Go

- Write in Go
  - https://youtu.be/LJvEIjRBSDA

## Before You Start

- https://www.youtube.com/watch?v=VDaMhtWNSQU&t=2s

## Syntax & Code Style

- init function; init()
  - init func is not highly recommended cos it makes global states.
  - what's this?: https://tutorialedge.net/golang/the-go-init-function/

- about interface and global state
  - https://peter.bourgon.org/blog/2017/06/09/theory-of-modern-go.html

- OOP
  - Is Go object-orientied?: https://flaviocopes.com/golang-is-go-object-oriented/

- Recommended project structure
  - https://github.com/golang-standards/project-layout

- Pkg style guide
  - https://rakyll.org/style-packages/

## Common Mistakes

- Field Name의 공개 범위에 주의
  - Basic concepts of capsulisation in Golang: https://yourbasic.org/golang/public-private/
  - 패키지 밖에서 사용하는 struct의 field name은 대문자로 시작해야 함.
  - **특히 JSON Parsing용 구조체를 만들 때 많이 하는 실수**
    - Don't make field names begin with a lowercase letter.

- `log.Fatal` with deferred functions
  - Don't use `log.Fatal` when a deferred function must run
  - alternatively, use `log.Panic`
  - ref : https://stackoverflow.com/a/17888654

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
  - i use this but it's more verbose than `gock`
  - https://github.com/jarcoal/httpmock
- `gock`
  - simpler
  - https://github.com/h2non/gock
  
## Good Articles

- porting from Java to Go
  - https://blog.kowalczyk.info/article/19f2fe97f06a47c3b1f118fd06851fad/lessons-learned-porting-50k-loc-from-java-to-go.html

## Famous Packages (for ref)

- go ethereum
  - https://github.com/ethereum/go-ethereum

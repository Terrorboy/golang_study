# Go를 공부하는 공간
- golang 첫 도전!


## go module
```bash
mkdir project && cd project
vi main.go
go mod init
go build
```


## main.go 예제
```go
package main // import "github.com/Terrorboy/go.hello"

import (
	"net/http"
	"github.com/labstack/echo"
)

func main() {
	e := echo.New()

	e.GET("/", func(c echo.Context) error {
		return c.String(http.StatusOK, "Hello, World!")
	})

	e.Logger.Fatal(e.Start(":1323"))
}
```
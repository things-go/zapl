# zapl zap logger with lumberjack

[![GoDoc](https://godoc.org/github.com/things-go/zapl?status.svg)](https://godoc.org/github.com/things-go/zapl)
[![Go.Dev reference](https://img.shields.io/badge/go.dev-reference-blue?logo=go&logoColor=white)](https://pkg.go.dev/github.com/things-go/zapl?tab=doc)
[![codecov](https://codecov.io/gh/things-go/zapl/branch/main/graph/badge.svg)](https://codecov.io/gh/things-go/zapl)
[![Tests](https://github.com/things-go/zapl/actions/workflows/ci.yml/badge.svg)](https://github.com/things-go/zapl/actions/workflows/ci.yml)
[![Go Report Card](https://goreportcard.com/badge/github.com/things-go/zapl)](https://goreportcard.com/report/github.com/things-go/zapl)
[![Licence](https://img.shields.io/github/license/things-go/zapl)](https://raw.githubusercontent.com/things-go/zapl/main/LICENSE)
[![Tag](https://img.shields.io/github/v/tag/things-go/zapl)](https://github.com/things-go/zapl/tags)

## Features

## Usage

### Installation

Use go get.
```bash
    go get github.com/things-go/zapl
```

Then import the package into your own code.
```bash
    import "github.com/things-go/zapl"
```

### Example

[embedmd]:# (_example/main.go go)
```go
package main

import (
	"go.uber.org/zap"

	"github.com/things-go/zapl"
)

func main() {
	l := zapl.New(zapl.WithLevel("debug"))
	zapl.ReplaceGlobals(l.Sugar().With(zap.String("main", "debug")))

	zapl.Debug("hello")
}
```

## References
- [go-lib-template](https://github.com/skanehira/go-lib-template)

## License

This project is under MIT License. See the [LICENSE](LICENSE) file for the full license text.

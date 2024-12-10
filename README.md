# Assert

[![Go](https://github.com/longbridge/assert/actions/workflows/go.yml/badge.svg)](https://github.com/longbridge/assert/actions/workflows/go.yml)

> 🍯 Requirement Go 1.18+ for Generics, lower Go version please use 0.x

Extends [stretchr/testify/assert](https://github.com/stretchr/testify/tree/master/assert) for add more useful methods.

- `assert.Equal` - asserts values equal, but ignore type.
- `assert.EqualHTML` - asserts HTML equal, ignore spaces.

## Installation

```bash
go get github.com/longbridge/assert
```

## Usage

```go
package some_test

import (
  "github.com/longbridge/assert"
)

func TestSomeMethod(t *testing.T) {
	assert.EqualHTML(t, "<p>Hello world</p><p>This is next line</p>", `
		<p>Hello world</p>
		<p>This is next line</p>
	`)
}
```

## License

MIT

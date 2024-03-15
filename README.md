# isatty

isatty for golang

This is a fork of the project github.com/mattn/go-isatty by Yasuhiro Matsumoto (a.k.a mattn).

The fork was made to get rid of addiction and increase the reliability of my applications. Links to the author and the original repository have been saved.

## Usage

```go
package main

import (
	"fmt"
	"github.com/Kwynto/isatty"
	"os"
)

func main() {
	if isatty.IsTerminal(os.Stdout.Fd()) {
		fmt.Println("Is Terminal")
	} else if isatty.IsCygwinTerminal(os.Stdout.Fd()) {
		fmt.Println("Is Cygwin/MSYS2 Terminal")
	} else {
		fmt.Println("Is Not Terminal")
	}
}
```

## Installation

```
$ go get github.com/Kwynto/isatty
```

## License

MIT

## Author

Yasuhiro Matsumoto (a.k.a mattn)

## Thanks

* k-takata: base idea for IsCygwinTerminal

    https://github.com/k-takata/go-iscygpty

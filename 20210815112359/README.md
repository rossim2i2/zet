# Tabbed Output in Golang

<https://pkg.go.dev/text/tabwriter>

The `TabWriter` package can be used in Go to to translate tabbed columns
into properly aligned text.

```Go
package main

import (
	"fmt"
	"os"
	"text/tabwriter"
)

func main() {
	w := new(tabwriter.Writer)

	// Format in tab-separated columns with a tab stop of 8.
	w.Init(os.Stdout, 0, 8, 0, '\t', 0)
	fmt.Fprintln(w, "a\tb\tc\td\t.")
	fmt.Fprintln(w, "123\t12345\t1234567\t123456789\t.")
	fmt.Fprintln(w)
	w.Flush()

	// Format right-aligned in space-separated columns of minimal width 5
	// and at least one blank of padding (so wider column entries do not
	// touch each other).
	w.Init(os.Stdout, 5, 0, 1, ' ', tabwriter.AlignRight)
	fmt.Fprintln(w, "a\tb\tc\td\t.")
	fmt.Fprintln(w, "123\t12345\t1234567\t123456789\t.")
	fmt.Fprintln(w)
	w.Flush()

}
```

```Output
a	b	c	d		.
123	12345	1234567	123456789	.

    a     b       c         d.
  123 12345 1234567 123456789.
```


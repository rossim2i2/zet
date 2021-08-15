# Golang `Fprint`, `Print` and `Sprint`

<https://pkg.go.dev/fmt#Fprint>

## Fprintln

> fprintln formats using the default formats for its operands and writes
> to w. Spaces are always added between operands and a newline is
> appended. It returns the number of bytes written and any write error
> encountered.

## Println

> Println formats using the default formats for its operands and writes to
> standard output. Spaces are always added between operands and a newline
> is appended. It returns the number of bytes written and any write error
> encountered.

## Sprintln

> Sprintln formats using the default formats for its operands and returns
> the resulting string. Spaces are always added between operands and a
> newline is appended.

F - Writes to `writer` (i.e. a file)
P - Writes to `stdout`
S - Returns resulting string



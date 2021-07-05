# User `recover` and `defer` in Go to Prevent Panics

If you `defer` from the main function, it propagates to all children as
well, thus covering the entire program. One useful way to do this is to
create a `trapPanic` function and defer to it within `main`.

``` go
func trapPanic() {
  p := recover()
  if p != nil {
    log.Println(p)
  }
}

func main () {
  defer trapPanic()
  fmt.Println("Hellow World")
}
```


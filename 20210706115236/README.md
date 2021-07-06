# Implement a JSON Stringer When Using Structs in Go

To make structs more readable in JSON format, add a stringer to your
code. A good habit to get into is adding this stringer whenever you
create a struct.

``` go
// String fulfills the Stringer interface
func (s State) String() string {
  byt, err := json.Marshal(s)
  if err != nil {
    return fmt.Sprintf(`{"Error":"%v"}`, err)
  }
  return string(byt)
}
```

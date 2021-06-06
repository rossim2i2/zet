# Use `go install` instead of `go get`

The `go get` command has been changed to only download the referenced
package and not install it. Using `go install` with an `@latest` at the
end of the URL is now the only way to download and install at the same
time.

```sh
go install github.com/rwxrob/cmd-pomo/pomo@latest
```

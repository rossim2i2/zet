# Never use brackets `[]` in POSIX

In POSIX shell scripts, brackets can be used as a replacement for the
`test` command.

```sh
if test -e "$1"; then
...
```

Is the same as:

```sh
if [ -e "$1" ]; then
...
```

However, using the brackets is very error prone.
1. If you forget the spaces inside the brackets, the script fails and is
   often difficult to detect when debugging larger scripts.
1. The code is not as readable. The command `test` is easy to read and
   follow. You know exactly what is going to take place.
1. It makes the code more searchable. Searching (grepping) for `test` is
   much easier than trying to find a bracket.
1. Leaves the code open for unsafe injections (globstar expansion).
  * To expand on this, in bash, the use of double brackets will not
    allow globstar expansion. Therefore, a popular "bashism" is to use
    the double brackets and not quote the variable. However, if you try
    to convert that piece of code to the POSIX standard, double brackets
    are not supported. This leads you to change the double brackets to
    single brackets. But unless you remember to quote the variable, you
    now opened the door or globstar expansion.

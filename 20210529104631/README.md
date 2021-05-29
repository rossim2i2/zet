# Using `set -e` in Shell Scripts

Adding this to the beginning of a shell script instructs the scrip to
automatically terminate the script if it encounters any instruction that
returns a false (non zero) status.

For example, take the following code:

```sh
#!/bin/sh

mdkir -p $HOME/.local/bin
```

If this directory already exists, the script will return an error
stating that the `mkdir` command failed (as the folder existed and could
not be created).

This can be wrapped in an `if` statement to check the return status and
tell the script to continue and ignore the returned error status.

However, adding `set -e` implies to exit the script upon a non zero
return code. Therefore, instead of including an `if` statement, we can
write something like the following, which will ignore the returned error
code and move on to the next instruction:

```sh
#!/bin/sh
set -e

mdkir -p $HOME/.local/bin || true
```

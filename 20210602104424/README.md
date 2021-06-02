# Vim, Bang Bang (!!) and Variations

I learned the !! trick from rwxrob, what he calls vimagic. Bang Bang,
will take the current line in vim, execute it against the command that
follows (i.e. bash or a call to a function), and replace the text with
the output of the command.

```sh
echo "Hello World!"
```

While a simple example, !!bash will execute that line of code in bash
and return the resulting text.

The real magic here is how you can also incorporate this into commands.

```sh
now
```

!!bash will replace now with the current date and time.

My confusion has always been where Rob refers how there is no need to
use visual mode. I did some digging and experimenting and found that:

```sh
:.! - Current line
:.,.+4! - Current line and four lines down
:.,$! - Current line to end of file
```

!! will select the current line
!} will select the current block of text/code.

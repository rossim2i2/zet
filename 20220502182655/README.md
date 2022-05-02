# New `log` Script for Brain Dumps

I just created a simple script to log quick thoughts and notes which may
require additional action. These entries will require additional though
as to next steps. These next steps can be:

* A new zet entry
* An action item (something that needs to be done)
* Something to defer and keep for future reference

```bash
#!/bin/bash

filename="$HOME/Private/daily.log"
logtext=`z isosec`

echo "$logtext $@" >> "$filename"

echo "LOGGED $@"
```

I need to determine if I should add functionality to remove items from
the log if additional work was performed on them. For now, that may
remain manual until I determine the optimal workflow.

    #braindump #zeroinbox #30days #writingchallenge

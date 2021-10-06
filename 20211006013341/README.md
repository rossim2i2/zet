# Finally Got FF14 Working on PopOS

I spent the better part of the day trying to get New World running on
Linux (to no avail). Others I've played ESO with recommended Final
Fantasy XIV to me, as that is the game they are currently playing.
Getting that to work was no small task either.

So I have a log of what to do, in the event I need to reload it or
someone else asks, the instructions provided by Maelstr0m on
protondb.com did the trick.

```
Launch the game -> stuck on FFXIV splash screen Close the game then :

cd .local/share/steam/steamapps/compatdata/39210/pfx/drive_c/users/steamuser/My Documents/My Games/FINAL FANTASY XIV - A Realm Reborn/

vim FFXIV_boot.cfg -> Switch value of BrowserType to 1

Launch the game again

Connect to your account (press enter and don’t click on log in otherwise it will crash)

Try to launch the game (for me I could select servers, but then got stuck on a black screen)

Back to the terminal (same location)

vim FFXIV.cfg

Change the value of CutsceneMovieOpening from 0 to 1

Launch the game again. It should work with no issue now.

Input:
Lag, Other
If you set frame rate limit (for me 144), the input will be EXTREMELY laggy and totally unusable. It took me a while to figure out that was the cause of the issue. I simply removed the limit and it runs perfectly.
```

<https://www.protondb.com/app/39210>

Tags:

    #linuxgaming #steam #ff14

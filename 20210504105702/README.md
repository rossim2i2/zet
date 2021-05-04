# CLI Script to Display To Do's Not Completed

I have been reading through the `git log` man pages and searching the
web for a way to mimic the GitHub GUI on the CLI. I want to see the
folder/file names, along with the commit message for my Zets and various
multi-calls; specifically my ToDo repo.

I have something working that shows both pieces of information, although
they have a new line break in between. Ideally this would all be on one
line. I made the commit message green to stand out and for easy
readability.

I also was able to filter the log for just additions which, for this use
case, works fine. However, when I move an item to the "Done" folder, the
original commit is still being displayed.

I had to get to sleep, but think deleting items as they are done may be
the answer. There is an argument I can pass to omit deletes and I can
even make a new script to show deletes if I need to view items that have
been completed.

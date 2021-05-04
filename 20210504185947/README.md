# CLI `ls` for `zet` To Do Repo

I finally got the script working to list outstanding to do items in the
repo, showing the commit message and folder/file name. I had to use `git
list` to get the list of files and pass them through xargs to `git log`.

I have a second version that passes that into 'sed' to remove new line
characters and keep each item on its own line. This may become useful as
the outstanding list continues to grow.

I added the `lstodo` script to my dotfile repo, but will incorporate
this into the overall zet/multi-call solution.

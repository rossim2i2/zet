# Docker Workspaces and Git Repos

I've been fascinated following rwxrob and his enthusiasm for Docker
containers. It is amazing how quickly you can spin up an instance of any
Linux distribution. He created his own `workspace` with all the tools
and configuration that meets his needs for his workflow.

As part of the "Beginners Boost", we will be setting up our own
workspaces. The appeal of containers is that they can be thrown away
without any effect to the host system. However, this causes an issue
when you want to save data. Any data saved in the container will be lost
when the container is thrown away.

Pushing this data to a Git repo seems to be the answer as it will keep
your data centralized and when you spin up a new container, you just
need to pull the repo and you are back where you left off.

This won't be possible at work though. I can't push work data to a
public Git repo (or even a private one hosted on Github or Gitlab.
However, I've heard that you can create a Git repo on a local folder or
a share drive. If I can create a repo on my personal share drive at
work, I can use `zet` and `log` as intended and create a real
Zettelkasten repository securely at work.

# Using SSH from Outside Network

To SSH into the home network, use Digital Ocean to create an OpenVPN or
a tunnel into the network. If possible, put the remotely accessible
system in an isolated network.

Doing it this way, you don't need to open any ports on the router. The
data is sent outbound to the tunnel, where you connect to the host
machine.

The hardest part of tunneling is ensuring the tunnel is active. You may
need to use CRON jobs to keep checking the status.

Thinking about it further, if I need to pull scripts or files that are
on my github, I can just install docker on the machine and start up a
Linux instance, clone my dotfiles, and install everything I need.

Another option is to just find a cheap, used laptop, install base Linux,
clone repos and have an exact replica of my home computer.

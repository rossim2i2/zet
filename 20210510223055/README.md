# Node Red and Mosquitto on Docker

Ran into an issue where Node Red could not connect to Mosquitto.
Originally, I had Mosquitto installed on metal and Node Red installed on
Docker. I figured the issue was the containerization of one and not the
other. So I tried adding both to docker. Same issue. Even when I put
them on the same network within Docker, they still couldn't communicate.

I found a stack that ran both applications and set up a new network. I
had the broker pointing to `localhost` and was getting the same error
message. However, when I switched it to the local IP address, it
connected right away and has been working fine since.

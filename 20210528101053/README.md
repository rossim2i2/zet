# Getting Govee Light strip Working in Node Red

----------------------------------------
Still not working. Need to debug more.
----------------------------------------

On the raspberry pi, under `~/.node-red/settings.js`, add the following
line to the `functionsGlobalContext` function. After saving the file,
restart the server/container.

```
Govee:require('Govee')
```

Also, ensure the proper node package is installed.

```
npm i node-govee-led
```

**Note - When running from a container...**

The settings.js file is located under
`usr/src/node-red/node_modules/node-red`


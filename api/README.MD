To Run this locally you need Docker and VirtualBox installed.
## First clone and build the VM
clone this repo
`cd iframe-test`
`docker build -t iframetest .`  the -t is for tagging, you can call that anything
Note the first time you build this it will take a long time. The second time it's all cached and will be faster.
If this is your first time using docker, I don't want it to come across slow for a first impression. ;)

### Run the VM
Assuming you've already built it, you don't need to again.
Run docker: `docker run -p 4500:4500 iframetest`  or whatever you've tagged it as when you built it

Now you should be able to go to http://192.168.99.100:4500
If that IP address doesn't work you can find the IP by running `docker-machine ip dev2`

### Other docker things
Run `docker-machine ls` to see machines running
Run `docker-machine ip dev2` to get the IP address, for me it's `192.168.99.100`
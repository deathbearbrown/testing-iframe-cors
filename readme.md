OH HAI.

This requires that you have docker installed and docker-machine cli.

I believe you still need to create the docker container, which I didn't add to that readme
`docker-machine create dev2 --driver virtualbox --virtualbox-disk-size "5000" --virtualbox-cpu-count 2 --virtualbox-memory "4112"`
then run:
`docker-machine env dev2`

Which will output:
```
export DOCKER_TLS_VERIFY="1"
export DOCKER_HOST="tcp://123.456.78.910:1112"
export DOCKER_CERT_PATH="/Users/user/.docker/machine/machines/dev2"
export DOCKER_MACHINE_NAME="dev2"
# Run this command to configure your shell:
# eval "$(docker-machine env dev2)"
```

and you run that `eval "$(docker-machine env dev2)"`

Once you get the api running get the IP address using `docker-machine ip dev2` and add it to your hosts file under api.whatever.com

All the code here is hardcoded to sue.com or api.sue.com, but you can change that, or not, whatevers.

I was running the site in www just with plain old python simple server on port localhost:8080, so whatever is your favorite server tool, use that.



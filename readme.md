## codecasts/rancher-deployer

Easily upgrade Rancher services.

#### Usage

You can build this image or customize and build your own, to upgrade a service, use it the following way:

Considering your Stack with ID `1e9` named `myapp-production` running on a environment ID `1a5`

Under this stack, you want to upgrade a service named `web`

```

docker run --rm \
    -e RANCHER_URL="http://my-rancher.com:8080/v1/projects/1a5" \
    -e RANCHER_ACCESS_KEY="my_api_key" \
    -e RANCHER_SECRET_KEY="my_api_secret \
    -e RANCHER_STACK_ID="1e9" \
    -e RANCHER_STACK_NAME="myapp-production" \
    -e RANCHER_SERVICE_NAME="web" \
    codecasts/rancher-deployer:latest
``` 

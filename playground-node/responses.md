Dockerize BOTH apps - the Python and the Node app.

1) Create appropriate images for both apps (two separate images!).
HINT: Have a brief look at the app code to configure your images correctly!

```bash
cd node-app/
docker build .
docker scan
```


2) Launch a container for each created image, making sure,
that the app inside the container works correctly and is usable.

```bash
docker run -p 4000:4000 playground-node
open http://localhost:3000
docker stop (container)
docker rm (container)
docker rmi (container)
```

3) Re-create both containers and assign names to both containers.
Use these names to stop and restart both containers.

4) Clean up (remove) all stopped (and running) containers,
clean up all created images.

```bash
docker stop [container]
docker rm [container]
docker rmi playground-node:latest
```
5) Re-build the images - this time with names and tags assigned to them.

```bash
docker build --tag playground-node:latest .
```

6) Run new containers based on the re-built images, ensuring that the containers
are removed automatically when stopped.

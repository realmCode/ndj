# NextJS and Docker

- node: v16.17.0
- npm: 8.19.2
- rootfs: alpine 3.15
- docker: 20.10.12, build e91ed57

A note about [alpine and node](https://github.com/nodejs/docker-node/tree/b4117f9333da4138b03a546ec926ef50a31506c3#nodealpine) which explains:

```Dockerfile
RUN apk add --no-cache libc6-compat
```



Enjoy!

### Local

#### Dev

`npm i && npm run dev`

### Docker Compose

`docker-compose up --build`

This will build and run your container locally :rocket:

### Traditional Docker Route

Build your containers for deploys:

MacOS/Linux

`./scripts/prod.sh`

Windows

`./scripts/prod.bat`

Now that your container is built, you can test it locally:

`docker run -p 3000:3000 nextjs-docker`

Now deploy :rocket:

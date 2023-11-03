# Website

This website is built using [Docusaurus 3](https://docusaurus.io/), a modern static website generator.

### Installation

```
$ yarn
```

### Local Development

```
$ yarn start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

You may also use Docker and docker-compose to run this locally.

```
$ docker-compose up --build -d
```

The site will be accessible at http://localhost:3000 and will mount your local files for hot-reload.

### Build

```
$ yarn build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

> [!NOTE]  
> Project is now archived due to switching to entirely static front end.

# About

This is the API for my website https://jordantucker.dev. You can find the repository
for the front end here: https://github.com/driedsponge/driedsponge.net.

### Deployment

This instance is configured with Docker & Docker Compose.
You will need to create a copy of `.env.example` and rename it to `.env`.
Be sure to set the proper environment variables.

The production and development configurations share the same Postgres database. They also share the
same credentials.

**This specific instance runs on port `1337`**.

#### Run the development instance:
```
docker compose --profile dev up -d --build
```
#### Run the production instance
```
docker compose --profile prod up -d --build
```
#### Don't forget to use the respective down command.
```
docker compose --profile dev down
```
or
```
docker compose --profile prod down
```
#### Running Commands Inside The Container
```
docker compose exec jordan-api 
```
```
docker compose exec jordan-api-prod
```
#### Data Transfer
```
docker compose exec jordan-api yarn strapi transfer --{from/to} {url}
```

# 🚀 Getting started with Strapi

Strapi comes with a full featured [Command Line Interface](https://docs.strapi.io/dev-docs/cli) (CLI) which lets you scaffold and manage your project in seconds.

### `develop`

Start your Strapi application with autoReload enabled. [Learn more](https://docs.strapi.io/dev-docs/cli#strapi-develop)

```
npm run develop
# or
yarn develop
```

### `start`

Start your Strapi application with autoReload disabled. [Learn more](https://docs.strapi.io/dev-docs/cli#strapi-start)

```
npm run start
# or
yarn start
```

### `build`

Build your admin panel. [Learn more](https://docs.strapi.io/dev-docs/cli#strapi-build)

```
npm run build
# or
yarn build
```

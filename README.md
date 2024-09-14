# stock-exchange

Hello, my name is Rastislav Chribik, and this is my self-presentational portfolio. In this space, I aim to showcase my coding skills through a simple stock application, which is composed of two core services: a user interface (UI) and an API.

## UI
- React application
- tailwind CSS framework
- typescript
- i18next for translations
- multiple components (chart)
- connection with API
- graphQL query to fetch stock history data from Yahoo Finance (it is stored to localstore to avoid calling API multiple times when page is reloaded)
- router to dynamically handle pages
- context, state
- very good test coverage (npm run test)
- linting (ESlint, prettier) configured (npm run lint-fix)
- Dockerfile

## API
- NestJS application
- typescript
- API endpoints to fetch stock data from Yahoo Finance
- graphQL resolver to fetch stock history data from Yahoo Finance
- request schema validation
- unit tests 100% coverage (npm run test)
- e2e tests coverage (npm run test:e2e)
- linting (ESlint, prettier) configured (npm run lint-fix)
- Dockerfile

## Stock Exchange
- docker compose

## What I would like to include next:
1. separate API to graphQL and API service
    - split API into two autonomous services to support microservices structure 
2. gRPC
    - switch API controllers to RPC methods that will be used by graphQL service to get data from Yahoo

## How to run the application?

1. Clone Repositories with Submodules

```bash
git clone --recurse-submodules git@github.com:digital-solutions-exercises/stock-exchange.git
```

2. Run the services (create images for stock-exchange-api and stock-exchange-ui) using docker compose

```bash
$ docker-compose up
```

3. Access http://localhost:3000/

## Add Submodules to the Parent Repository
```bash
git submodule add git@github.com:digital-solutions-exercises/submodule-repo-api.git ./submodules/submodule-repo
```

## Updating Submodules

### Pull the latest changes from the submodule’s repository:
```bash
cd submodules/example-submodule
git pull origin main
```

### Return to the main repository and commit the updated submodule:
```bash
cd ../..
git add modules/example-submodule
git commit -m "Updated example-submodule"
git push origin main
```

## Removing a Submodule
```bash
git rm --cached ./submodules/submodule-repo
rm -rf ./submodules/submodule-repo
```

### Commit the changes:
```bash
git add .gitmodules
git commit -m "Removed submodule"
git push origin main
```
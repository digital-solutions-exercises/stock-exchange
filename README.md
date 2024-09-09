# stock-exchange

## How to run the application?

1. Run the services (create images for stock-exchange-api and stock-exchange-ui) using docker compose

```bash
$ docker-compose up
```

2. Access http://localhost:3000/

## Cloning Repositories with Submodules
```bash
git clone --recurse-submodules git@github.com:digital-solutions-exercises/stock-exchange.git
```

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
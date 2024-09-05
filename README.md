# stock-exchange

## Add Submodules to the Parent Repository
```bash
git submodule add https://github.com/username/submodule-repo.git ./submodules/submodule-repo
```

## Working with Submodules
```bash
git clone git@github.com:digital-solutions-exercises/stock-exchange.git
cd stock-exchange
git submodule init
git submodule update
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

## Cloning Repositories with Submodules
```bash
git clone --recurse-submodules https://github.com/username/your-parent-repo.git
```
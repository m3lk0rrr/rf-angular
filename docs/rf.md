# [angular]


## 0. preparations:

```bash
nvm install --lts
npm install -g @angular/cli

ng new ag-tests
# regular css
# no ai tools
# no SSR
npm start
# OK, ctrl-c
git status
# empty, OK
```

vs cycle
```bash
code .
# install Angular Language Server
```


angular 21.1 (latest by ng new)
with 7.8 rxjs, 5.9 typescript, 4.0 vitest

"default settings tsconfig"
```json
"compilerOptions": {
    "strict": true,
    "noImplicitOverride": true,
    "noPropertyAccessFromIndexSignature": true,
    "noImplicitReturns": true,
    "noFallthroughCasesInSwitch": true,
    "skipLibCheck": true,
    "isolatedModules": true,
    "experimentalDecorators": true,
    "importHelpers": true,
    "target": "ES2022",
    "module": "preserve"
},
```


## 1. testing out hot-reload fast-feedback editing by modifiying app.html slightly. OK


## 2. copy the src/app/app.html in a new ./_DRAFTS_/ folder for backup.


## 3. cleaup the original with

```html
<main>
  <h2>Hi!</h2>
</main>

<router-outlet />
```


## 4. fix the tests:
image


## 5. commit as starting base


## 6. edit feedback loop with chrome/(ium) seems ok. vs code ok.


## 7. add new github remote for logging

```bash
# create new repo in github, added ssh keys

# check for any credentials or sensitive informations
# - no keys, the names are mostly scrubed (rf as namespace)

# register remote locally
git remote add origin git@github.com:m3lk0rrr/rf-angular.git
# fetch remote for merging already existing licence and remote history
git fetch origin
# merge the remote local branches
git merge origin/main --allow-unrelated-histories
# rename the local branch (it was created as 'master')
git branch -M main
# push it to github
git push -u origin main
```


## 8. add sonarcube (sonarsource.sonarlint-vscode) for code quality to vscode

- ensuring its not connected (offline) and shows warnings


## 9. check for linter

```sh
npm ls eslint # empty
npx ng lint # wants install
ng lint # wants install

# add it manually
ng add angular-eslint
```

- ensure `eslint.config.js` exists
- install ESLint (dbaeumer.vscode-eslint)
- reload vscode

```ts
const x = 42;
```
should be marked as unused variable


## 10. add eslint config, commit (,push)

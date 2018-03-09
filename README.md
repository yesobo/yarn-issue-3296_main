### To replay https://github.com/yarnpkg/yarn/issues/3296

***
yarn install
rm -rf node_modules
yarn install
***


### Issue details
- Resolutions
  - When yarn install --flat for the first time, yarn only records the version number into *"resolutions"* on *package.json*.
  - On the next yarn install, yarn fails becouse it reads resolution as if it were a published npm package.

- yarn.lock
  - Contrary to mentioned on issue 3296 yarn.lock resolved version is OK
---
title: Welcome to my blog
---

## Running the app locally

1. To install all project dependencies, run:

```shell
npm i
```

2. To bundle the page model for local development, run:
```shell
npm run package:apps -- --applications business-banking-app --configuration production
```
```shell
npm run bundle-home-page:business
```

3. To start your application, run:
Local environment:
```shell
npm start
```
Proxy environment:
```shell
npm run start:proxy
```

### Enabling mocks
To enable mocks, open browser console and run:
```shell
localStorage.setItem('enableMocks', true)
```

## Create library
Generate widget
```shell
npx nx g @nrwl/angular:library widgets/<widget-name> --skipPackageJson --skipModule --standaloneConfig
```
Generate component
```shell
npx nx g @nrwl/angular:compoent <component-name> --style=none
```
Generate service
```shell
npx nx g @nrwl/angular:service <service-name>
```
Generate directive
```shell
npx nx g @nrwl/angular:directive <directive-name>
```
Generate pipe
```shell
npx nx g @nrwl/angular:pipe <pipe-name>
```

## Run unit test
Test widget
```shell
nx run <widget-name>:test --codeCoverage --watch=false --detectOpenHandles
```

Test whole project
```shell
npm run test
```

## Run translation command
This apps is a dual language app with English and Vietnamese. To update the translation after changes to any widget, please run below command.
```shell
npm run xi18n-all
```
it will update the translations in the `xlf` files for the newly added element


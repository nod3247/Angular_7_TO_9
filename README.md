# Angular_7_TO_9

Update automatically
ng update @angular/cli @angular/core
 
Update manually
Angular CLI (global)
npm install @angular/cli@9.0.0 -g
Angular dependencies (local)
npm install @angular/animations@9.0.0 @angular/common@9.0.0 @angular/compiler@9.0.0 @angular/core@9.0.0 @angular/forms@9.0.0 @angular/platform-browser@9.0.0 @angular/platform-browser-dynamic@9.0.0 @angular/platform-server@9.0.0 @angular/router@9.0.0
 
Optional; if you use Material Design:
npm install @angular/cdk@9.0.0 @angular/material@9.0.0
Angular dev dependencies (local)
npm install @angular-devkit/build-angular@0.900.1 @angular/compiler-cli@9.0.0 @angular/cli@9.0.0 @angular/language-service@9.0.0 --save-dev
All other related dependencies (local)
npm install core-js@latest zone.js@latest rxjs@latest
And related dev dependencies (local)
npm install @types/jasmine@latest @types/node@latest codelyzer@latest karma@latest karma-chrome-launcher@latest karma-cli@latest karma-jasmine@latest karma-jasmine-html-reporter@latest jasmine-core@latest jasmine-spec-reporter@latest protractor@latest tslint@latest webpack@latest rxjs-tslint@latest --save-dev

Upgrade Typescript
npm i typescript@3.1.6 --save-dev --save-exact
npm i typescript@(your typescript version which angular give error) --save-dev --save-exact

In tsconfig.json
{
  "compileOnSave": false,
  "compilerOptions": {
    "baseUrl": "./",
    "outDir": "./dist/out-tsc",
    "sourceMap": true,
    "declaration": false,
    "module": "esnext", // update this line

"target": "es2015",
Update LoadChildren Syntax

   {path:'page', loadChildren:() => import('./page/page.module').then(m=>m.PageModule)},

In case you get errors here, please remove package-lock.json and node_modules and run a npm install .

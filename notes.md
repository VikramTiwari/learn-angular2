## Getting Started Notes
==

### Set up dev environment
Along with the above, set up the dev environ using the following:
1. Install Typescript
```
npm install -g tsd@^0.6.0
tsd install angular2 es6-promise rx rx-lite
```
2. Run the Typescript compiler
```
npm install -g typescript@^1.5.0-beta
tsc --watch -m commonjs -t es5 --emitDecoratorMetadata app.ts
```
3. Import Angular: Inside your main application file, import type definitions for Angular
```
/// <reference path="typings/angular2/angular2.d.ts" />
```
4. Use a simple server for running the app
For Python users: ```python -m SimpleHTTPServer 8000```
For NodeJS users: ```server```

## Steps to create any Angular app
1. Create an entry point HTML file where users will start
2. Load the Angular library at the top of the file
3. Make a root component for your application
4. Bootstrap Angular

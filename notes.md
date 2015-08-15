# Getting Started Notes

## Set up dev environment
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

## Explanations

#### Its all tree
Angular apps are a tree of components. We defined a root component ```AppComponent``` which will be top level container for the app. Its job is to provide a location in ```index.html``` file where app will be rendering through its element ```<my-app>```. Root component loads initial template for application that will load other components to perform functions for applications (menus, views, forms).
#### Annotations
A component annotation describes details about the component. Identified by ```@``` sign. ```@Component``` defines the HTML tag by specifying its CSS selector. ```@View``` defines the HTML that represents the component. To use external template, specify a ```templateUrl``` property with path to HTML file.
#### import vs window.angular
TypeScript supports ES6 module loading syntax, for JavaScript code. Pick only what you need for your app.

#### Interpolation
Method for binding text into templates is through interpolation. Angular automatically binds the data with template by calling a new on your Component.

#### Use NgFor on view on arrays

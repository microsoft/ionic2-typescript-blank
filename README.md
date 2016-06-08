# Ionic 2 Blank Template

An application using Apache Cordova, Ionic2 Framework, and Typescript. Currently supporting iOS, Android and Windows 10.

## Important!
To learn more about Tools for Apache Cordova, visit this [link](https://taco.visualstudio.com/).

## Table of Contents
 - [Requirements](#requirements)
 - [Getting Started](#getting-started)
 - [File Structure of App](#file-structure-of-app)
 - [Things to keep in mind](#things-to-keep-in-mind)
 - [File Structure of App](#file-structure-of-app)

## Requirements
1. node.js
2. Cordova and Ionic2 - npm install cordova ionic@beta
3. TypeScript - npm install typescript
4. IMPORTANT UPDATE. Ionic 2 has released Beta 7, that uses Angular 2 RC1. This version strictly requires NPM 3.x, so you will need to update the web tools by downloading this [VSIX](https://visualstudiogallery.msdn.microsoft.com/32f1fa1b-cdd5-4bd3-8f51-cd8f099f46bc).

## Getting Started

With VS Code:
* Clone this repository.
* Run `npm install` from the project root.
* Add android / iOS / windows platform to your project by running `ionic platform add <platform name>` in a terminal from your project root.
* Build the project by running gulp tsc and then `ionic build <platform name>`
* Deploy to device or emulator by running `ionic run <platform name>` or `ionic emulate <platform name>`. Or deploy to browser bu simply running `ionic serve`
* Success

    ** Note: To improve your Cordova development workflow, install [VS Code Cordova extension](https://marketplace.visualstudio.com/items?itemName=vsmobile.cordova-tools). 
* Launch the VS Code Command Palette – (Ctrl+Shift+P on Windows, Cmd+Shift+P on Mac) – and type the following command and hit Enter: 
> ext install cordova-tools

With Visual Studio:
* Clone this repository.
* Open the ionic2-ts-blank.sln in Visual Studio.
* Install npm packages by going to your Solution Explorer -> Dependencies -> npm and clicking on 'Restore Packages'. 
* Open Task Runner window by pressing Ctrl+Alt+Bkspce. 

    ** Note: It is important that the task runner window be open in VS while building the project. You can also use "gulp watch" task to enable live reload in browser based debugging scenarios.    

* Build the project and deploy it on Ripple or an android emulator.  
* Success

## Things to keep in mind

Ionic 2 is Beta, and so is Angular 2. There are number of things being actively worked on that aren't quite ready yet. Here are some things to keep in mind as you try out Ionic 2 and Angular 2:

### Missing Ionic 1 features

We are currently working on completing a few core Ionic 1 features:

- Collection repeat (known as Virtual Scrolling in v2) is not quite ready

### Current Angular 2 known issues:

- Angular 2 is still in alpha and is not production ready
- Angular team has first focused on developing what the core of Angular 2 "is"
- Angular 2 filesize has not been optimized for minification yet
- Angular 2 bootstrap time has not been optimized yet
- As Angular 2 reaches beta there will be significant performance improvements


### ES6/Typescript

- Ionic's source is written using [Typescript](http://www.typescriptlang.org/)
- Ionic apps can be written in ES6 or TypeScript
- Typescript is an optional feature to be used at the developers discretion
- Ionic 2 starters come with the necessary build tools to transpile both ES6 and Typescript


### CSS Attribute Selectors:

- Simple
- Smaller markup
- Easier to read and understand
- [Not an issue](https://twitter.com/paul_irish/status/311610425617838081) for today's mobile browsers
- No performance impacts have been found


### Distribution

 - [npm: ionic-framework](https://www.npmjs.com/package/ionic-framework)


#### Webpack

- Starter project is already setup to build Ionic using [Webpack](http://webpack.github.io/)


## File Structure of App

```
ionic2-ts-blank/
├── app/                               * Working directory
│   ├── pages/                         * Contains all of our pages
│   │   └── home/               
│   │        ├── home.html            * home template
│   │        ├── home.ts              * home code
│   │        └── home.scss            * home stylesheet  
│   │
│   ├── theme/                         * App theme files
│   │   ├── app.core.scss              * App Shared Sass Imports
│   │   ├── app.ios.scss               * iOS Sass Imports & Variables
│   │   ├── app.md.scss                * Material Design Sass Imports & Variables
│   │   ├── app.variables.scss         * App Shared Sass Variables
│   │   └── app.wp.scss                * Windows Sass Imports & Variables
│   │
│   ├── app.html                       * Application template
│   └── app.ts                         * Main Application configuration
│
├── node_modules/                      * Node dependencies
|
├── platforms/                         * Cordova generated native platform code
|
├── plugins/                           * Cordova native plugins go
|
├── resources/                         * Images for splash screens and icons
|
├── www/                               * Folder that is copied over to platforms www directory
│   │   
│   ├── build/                         * Contains auto-generated compiled content
│   │     ├── css/                     * Compiled CSS
│   │     ├── fonts/                   * Copied Fonts
│   │     ├── js/                      * ES5 compiled JavaScript
│   │     ├── pages/                   * Copied html pages
│   │     └── app.html                 * Copied app entry point
│   │
│   └── index.html                     * Main entry point
|
├── .editorconfig                      * Defines coding styles between editors
├── .gitignore                         * Example git ignore file
├── config.xml                         * Cordova configuration file
├── ionic.config.json                  * Ionic configuration file
├── LICENSE                            * Apache License
├── package.json                       * Our javascript dependencies
├── gulpfile.js                        * Contains gulp tasks
├── ionic2-ts-blank.sln                * VS solution
├── ionic2-ts-blank.jsproj        
└── README.md                          * This file
```
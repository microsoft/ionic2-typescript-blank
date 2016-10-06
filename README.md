# Ionic 2 Blank Template with TypeScript

>Note. This template is based on Ionic 2 Beta 10.

A template to create Ionic 2 apps with Visual Studio tools for Apache Cordova using TypeScript

## Table of Contents
 - [Visual Studio Requirements](#visual-studio-requirements)
 - [VSCode Requirements](#vscode-reqirements)
 - [Getting Started](#getting-started)

## Visual Studio Requirements
* [Visual Studio 2015 Update 3](https://download.microsoft.com/download/4/8/f/48f0645f-51b6-4733-b808-63e640cddaec/vs2015.3.exe)
* [Tools for Apache Cordova Update 10](http://taco.visualstudio.com/en-us/docs/install-vs-tools-apache-cordova/)
* [Microsoft ASP.Net and WebTools](https://visualstudiogallery.msdn.microsoft.com/c94a02e9-f2e9-4bad-a952-a63a967e3935)

## VSCode Requirements
* A recent version of Node/NPM 
* A global installed version of  Cordova,Ionic, and TypeScript npm packages: `npm i -g cordova ionic@beta typescript`

## Getting Started
Once you have your first project based on this template/repo created, you should follow the next steps:

### Restore Npm Packages
VSCode will depend on you to execute `npm install` from the root folder.

Visual Studio should start the restore process as soon the project is opened, you should see how the Dependencies node in Solution Explorer shows a message saying "Restoring..",
you can always invoke the restore process manually with `RightClick->Restore Packages`

To verify that the packages are completely restored you can check that the folder `www\build` contains some folders.
> Note. Visual Studio shows the restore log in the Output Window `Ctrl+Alt+O` under the Npm/Bower category.  

### Run Gulp Tasks
Ionic uses [Gulp](http://gulpjs.com/) to perform some tasks like [Sass](http://sass-lang.com/), and TypeScript compilation to process your source code and produce the output in the `www` folder.

Visual Studio 2015 includes a Task Runner Explorer that will show you all the available tasks to execute from the UI. 
You can access the Task Runner Explorer from the Menu: `View->Other Windows-Task Runner Explorer` or with the shortcut `Ctrl+Alt+Bkspce`  

>Note: To ensure that the default tasks are executed before the VS build, we configured the Task Runner Explorer binding the default task to the BeforeBuild event, however you can customize this setting to match your needs (e.g. Binding watch to project opened)

To execute this tasks from the CLI you can:

1. Have a global installation of gulp, and run `gulp build`
2. Use the local installed version `node_modules\.bin\gulp build`
3. Use the npm script: `npm run build`

> Note: If VS is unable to show the tasks, you can check the log in the Ouput window under the Task Runner Explorer Logs category.

### Usual Cordova development Workflow
Once you have all the packages restored, and the Gulp tasks executed, you can use your favorite cordova workflow:

* [Cordova Getting Started](http://cordova.apache.org/#getstarted)
* [Ionic Getting Started](http://ionicframework.com/getting-started/)

#### Live Reload
Ionic cli offers the `ionic serve` command to implement a Live Reload development workflow, you can obtain similar results executing the gulp task `watch` 
and using the Live Reload capabilities of the Ripple Emulator

## Code of conduct
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
# Introduction

The purpose of this project is to bundle together Angular 5 and Electron for developing desktop applications. 
The project offers the following features:

- TypeScript, SASS and Hot Reload support.
- A local development environment for both Web & Electron
- Create a web app ready for deployment in a production environment
- Package an Electron app into an executable file for Linux, Windows or Mac

The project core dependencies are:

- Angular v5.2.0
- Angular-CLI v1.7.3
- Electron v1.8.4
- Electron Builder v20.8.1

## Getting Started

Clone this repository locally :

``` bash
git clone https://github.com/maximegris/angular-electron.git
```

Install dependencies with npm :

``` bash
npm install
```

To gain support of the Angular CLI :

``` bash
npm install -g @angular/cli
```

To start the application in the web browser & Electron in a local development environment with hot reload:
``` bash
npm start
```

## Managing the Environment

The application code is managed by `main.ts`. 
The app is currently set to to run in a browser (http://localhost:4200) and an Electron window.  
The Angular component contains an example of Electron and NodeJS native lib import.  
You can deactivate "Developer Tools" by commenting out `win.webContents.openDevTools();` in `main.ts`.

- Using local variables :  `npm start` or `cross-env ENV=local npm start`
- Using development variables :  `cross-env ENV=dev npm start`
- Using production variables  :  `cross-env ENV=rod npm start`

## Supported Commands

|Command|Description|
|--|--|
|`npm start`| Starts the app for development in both the browser & Electron |
|`ng serve`| Starts the app for development in the browser |
|`npm run build`| Builds the app into the `/dist` folder. |
|`npm run build:prod`| Builds the app with Angular aot into the `/dist` folder |
|`npm run electron:local`| Builds the application and starts electron
|`npm run electron:linux`| Builds the application and creates an app consumable on a linux system |
|`npm run electron:windows`| Builds the application and creates an app consumable in windows 32/64 bit systems (when run on a Windows OS) |
|`npm run electron:mac`|  Builds the application and generates an `.app` file that can be run on Mac (when run on a Mac OS) |
|`npm test`| Executes all unit tests in the browser |
|`npm run e2e`| Executes all e2e tests in the browser |

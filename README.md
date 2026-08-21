# my-electron-app
cross-platform desktop app with electron

References:
* [Tutorial](https://www.electronjs.org/docs/latest/tutorial/tutorial-first-app)


## 1. Setup
```shell
$ npm i -g yarn@latest
$ npm i -g --allow-scripts=yarn

$ yarn -v
$ mkdir my-electron-app
$ cd my-electron-app/
$ yarn init
$ cat package.json 
$ yarn add electron --dev
$ yarn run start
```

## 2. Preload Script
A preload script contains code that runs before your web page is loaded into the browser window. It has access to both DOM APIs and Node.js environment, and is often used to expose privileged APIs to the renderer via the `contextBridge` API.

Because the main and renderer processes have very different responsibilities, Electron apps often use the preload script to set up inter-process communication (IPC) interfaces to pass arbitrary messages between the two kinds of processes.
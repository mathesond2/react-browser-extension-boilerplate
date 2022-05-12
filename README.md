# Browser Extension
This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app) with some minor modifications for handling `node_modules` and build output paths via [Craco](https://www.npmjs.com/package/@craco/craco)

literally how this was built:
1. add create-react-app with TS template
2. add manifest.json and assets in `/public`
3. add watch script and associated command in `package.json` for live reload
4. add background script (you prob might use it in a extension)
5. add craco npm package, associated config file, and modify build script `package.json`

#### Notes
* There's currently an incompatibility between craco and the latest [react-scripts](https://www.npmjs.com/package/react-scripts) version (5.0.1 as of 05/12/22) per this [issue](https://github.com/gsoft-inc/craco/issues/378). Repo will be updated upon finding a fix, though react-scripts version 4.0.3 will suffice for now.

* This extension boilerplate was initally derived from [this article](https://mmazzarolo.medium.com/developing-a-browser-extension-with-create-react-app-b0dcd3b32b3f), a special thank you to Matteo Mazzarolo.🎖

## Installation
1. cd into dir and `npm i`
2. `npm run watch`
3. navigate to `chrome://extensions/`, toggle 'developer mode', and hit 'load unpacked' button, and select `/build`.
4. code --> hit save --> see changes upon re-clicking extension icon.
5. run `npm run build` when ready, outputs to `/build`. you'll have to zip the folder to submit it to Chrome store.


## Available Scripts

In the project directory, you can run:
### `npm run watch`

This script allows for hot reload functionality during development, creating a build folder at `/build`, changes there are watched and code re-compiled from the watch script (scripts/watch.js)
### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `/build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

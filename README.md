# Browser Extension
This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app) with some minor modifications for handling build output paths via [Craco](https://www.npmjs.com/package/@craco/craco).

How this was built:
1. add create-react-app with TS template
2. add V3 manifest.json and assets in `/public`
3. add watch script and associated command in `package.json` for live reload capability
4. add background script (you may use this within your extension)
5. add craco npm package, associated and associated config file, modify build script to use craco in `package.json`.

#### Notes
* There's currently an incompatibility between craco and the latest [react-scripts](https://www.npmjs.com/package/react-scripts) version (5.0.1 as of 05/12/22) per this [issue](https://github.com/gsoft-inc/craco/issues/378). Repo will be updated upon finding a fix, though react-scripts version 4.0.3 will suffice for now.

* This extension boilerplate was initally derived from [this article](https://mmazzarolo.medium.com/developing-a-browser-extension-with-create-react-app-b0dcd3b32b3f), a special thank you to Matteo Mazzarolo. 🤝

## Installation
1. `npm i`
1. `npm run build`
1. `npm run watch`
1. navigate to `chrome://extensions/`, toggle 'developer mode', and hit 'load unpacked' button, and select `/build`.
1. code --> hit save --> see changes upon re-clicking extension icon.
1. when ready, run `npm run build` and zip the folder to prepare it for Chrome store submission.

## Available Scripts

In the project directory, you can run:
### `npm run watch`

This script allows for hot reload functionality during development, creating a build folder at `/build`, changes there are watched and code re-compiled from the watch script (scripts/watch.js)
### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `/build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance. In this step we use the craco package in order to account for background scripts, but you can modify it for content scripts as well.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

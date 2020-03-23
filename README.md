This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `npm run build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify

## Development Steps ###

Tell git to use a LF end of line (EOL) character so that EOL war is ended.
I do this so GitHub can stop converting end of line characters, and I use editors that behave properly.
This is a choice that dev teams can make for themselves if desired.

```
git config --global core.autocrlf false
```

### Create
```
npm create-react-app sudoku

# Add the .editorconfig file
# Add components library
npm install @material-ui/core --save
npm install typeface-roboto --save
npm install @material-ui/icons --save

# Add to index.js
import 'typeface-roboto';
```

### Remove unused code
* In index.js remove serviceWorker references
* In index.css remove unused styles
* in App.js remove all but the outer div
* In App.js remove all unused imports
* In App.css remove unused styles

### Add Components

```
cd src
mkdir components

# Add routing for menu items
npm install react-router-dom --save
```

* Add file apptoolbar.js (see it for details)
* In App.js add
```
import AppToolBar from './components/apptoolbar';`
...
<AppToolBar />
```

# GitHub Pages Deployment

```
npm install gh-pages --save-dev

# Edit package.json top level
"homepage": "http://{user}.github.io/{project}"

# Now add to the scripts section
"predeploy": "npm run build",
"deploy": "gh-pages -d build"
```

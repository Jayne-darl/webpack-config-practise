# CONFIGURING WEBPACK FOR PROJECT BUNDLING
1. Create a folder for the project

2. Install development packages 
  * `npm install --save-dev webpack`[See webpack npm doc for more](https://www.npmjs.com/package/webpack)
  * `npm install --save-dev webpack-dev-server` This package is a development server that provides live. reloading [webpack-dev-server npm doc](https://www.npmjs.com/package/webpack-dev-server)
  * `npm install --save-dev webpack-cli` Webpack CLI provides a flexible set of commands for developers to increase speed when setting up a custom webpack project.[learn more](https://www.npmjs.com/package/webpack-cli)
  * `npm install --save-dev eslint` is a tool for identifying and reporting on patterns found in ECMAScript/JavaScript code, with the goal of making code more consistent and avoiding bugs. [Read More](https://eslint.org/docs/user-guide/getting-started)
  * `npm install --save-dev @babel/core @babel/preset-env @babel/preset-react babel-loader ` Babel is used for transpiling ES6 code to ES5 so that every browser can understand it. It can also tranpile JSX using the react preset. [Read More](https://babeljs.io/docs/en/)
  * `npm install --save-dev babel-eslint` for linting all valid babel code with eslint; use case is types or experimental features not supported in eslint itself yet[Read More](https://www.npmjs.com/package/babel-eslint)

3. Install project dependencies: you can install depending on what you are building and the library or framework you are working with. I will use react, so i will install react and react-dom
  * `npm install react react-dom`

4. Create a  dist folder and create an index.html inside it. the body of the index file should have a script tag
` <script src='/bundle.js'></script>`

5. Create a src folder and an index.js file inside it

6. Create a config file and write this
```const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'main.js',
    path: path.resolve(__dirname, 'dist'),
  },
};
```

Visit [webpack documentation](https://webpack.js.org/guides/getting-started/) for better understanding. You can add other configuration as you deem fit, see webpack.config.js to see a sample.

7. Change the start key in the script to 
```webpack-dev-server --config ./webpack.config.js --mode development``` to be able to compile the project and start listening at a port.

8. Run `npm start` to start server, once it is successfully compiled, copy the link to hte port the project is running, paste on your browser.
Hurray!!! you have successfully configured webpack for your project, code away... :smile:


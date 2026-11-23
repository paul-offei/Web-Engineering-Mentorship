# React 
- [React](https://react.dev/)

## Environmental Setup

we will set up the initial structure of our React application by creating two main folders: `client` and `server`. The `client` folder will contain our React application, while the `server` folder will be responsible for serving the application to the browser.

Since we have not started implementing our main backend server, we will use a lightweight HTTP server called `http-server` to serve our React application.

## 1. Create the Project Structure

First, create the main project directory and navigate into it. Then create the `client` and `server` folders.

```bash
mkdir react-project
cd react-project
mkdir client server
```

Our initial project structure should look like this:

```text
react-project/
├── client/
└── server/
```

## 2. Initialize the Server Project

Navigate into the `server` folder and initialize a new Yarn project.

```bash
cd server
yarn init -2
```

This creates a `package.json` file, which contains information about our project, dependencies, and scripts.

Next, install `http-server` as a development dependency.

```bash
yarn add -D http-server
```

We use `http-server` because it provides a simple way to serve static files over HTTP without implementing a backend server ourselves.

## 3. Create the HTML Entry Point

Inside the `server` folder, create an `index.html` file.

```bash
touch index.html
```

Open the file and add the following HTML:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>React Application</title>

    <script src="./spa.bundle.js"></script>
</head>
<body>
    <div id="root"></div>
    <div>Hello World</div>
    <script>
        spa.main();
    </script>
</body>
</html>
```

The `spa.bundle.js` file contains our bundled React application and is loaded inside the `<head>` tag. The `<div id="root"></div>` element provides the mounting point where React will render the application. Finally, `spa.main()` initializes the Single Page Application.

**Note:** The `spa.bundle.js` file will be generated from our client-side application during the build process and must be available at the specified path.

## 4. Configure the Server Script

Open the `package.json` file inside the `server` folder and add the following script under the `scripts` section:

```json
"scripts": {
    "backend": "http-server -p 5000"
}
```

The `http-server -p 5000` command starts the HTTP server on port `5000`. By defining it as a Yarn script called `backend`, we can conveniently start our server using Yarn.

## 5. Start the Server

To start the server, make sure you are inside the `server` directory and execute:

```bash
yarn backend
```

Once the server starts successfully, open your browser and navigate to:

```text
http://localhost:5000
```

The browser will load `index.html`, which in turn loads the React application bundle and initializes the application using `spa.main()`.

To stop the server, press `Ctrl + C` in the terminal.

## Final Project Structure

At this stage, our project should have the following structure:

```text
react-project/
├── client/
│   └── (React application source files)
│
└── server/
    ├── index.html
    ├── package.json
    └── (spa.bundle.js - generated build file)
```

We have now established the basic server environment for our React application. In the next stage, we will focus on setting up the client-side React application and generating the `spa.bundle.js` file that the server will deliver to the browser.


# Setting Up the React Application

In this practical session, we will continue setting up our React application. Our project consists of two main folders: `client` and `server`. The `server` folder serves the application to the browser, while the `client` folder contains the React application and its development tools.

# Part 1: Setting Up the Server

Since we have not started implementing our main backend server, we will use a lightweight HTTP server called `http-server` to serve our React application.

## 1. Create the Project Structure

First, create the main project directory and navigate into it. Then create the `client` and `server` folders.

```bash
mkdir react-project
cd react-project
mkdir client server
```

Our initial project structure should look like this:

```text
react-project/
├── client/
└── server/
```

## 2. Initialize the Server Project

Navigate into the `server` folder and initialize a new Yarn project.

```bash
cd server
yarn init -2
```

This creates a `package.json` file, which contains information about our project, dependencies, and scripts.

Next, install `http-server` as a development dependency.

```bash
yarn add -D http-server
```

We use `http-server` because it provides a simple way to serve static files over HTTP without implementing a backend server ourselves.

## 3. Create the HTML Entry Point

Inside the `server` folder, create an `index.html` file.

```bash
touch index.html
```

Open the file and add the following HTML:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>React Application</title>

    <script src="./spa.bundle.js"></script>
</head>
<body>
    <div id="root"></div>

    <script>
        spa.main();
    </script>
</body>
</html>
```

The `spa.bundle.js` file contains our bundled React application and is loaded inside the `<head>` tag. The `<div id="root"></div>` element provides the mounting point where React will render the application. Finally, `spa.main()` initializes the Single Page Application.

**Note:** The `spa.bundle.js` file will be generated from our client-side application during the build process and must be available at the specified path.

## 4. Configure the Server Script

Open the `package.json` file inside the `server` folder and add the following script under the `scripts` section:

```json
"scripts": {
    "backend": "http-server -p 5000"
}
```

The `http-server -p 5000` command starts the HTTP server on port `5000`. By defining it as a Yarn script called `backend`, we can conveniently start our server using Yarn.

## 5. Start the Server

To start the server, make sure you are inside the `server` directory and execute:

```bash
yarn backend
```

Once the server starts successfully, open your browser and navigate to:

```text
http://localhost:5000
```

To stop the server, press `Ctrl + C` in the terminal.

# Part 2: Setting Up the Client

Now that we have configured our server, let us set up the client-side application using React, TypeScript, Babel, and Webpack.

## 6. Initialize the Client Project

Navigate back to the main project directory and enter the `client` folder.

```bash
cd ..
cd client
```

Initialize a new Yarn project:

```bash
yarn init -2
```

This creates a `package.json` file for managing our client-side project and its dependencies.

## 7. Install and Configure TypeScript

First, install TypeScript as a development dependency.

```bash
yarn add -D typescript
```

Next, initialize the TypeScript compiler configuration.

```bash
yarn tsc --init
```

This generates a `tsconfig.json` file, which allows us to configure how TypeScript checks and compiles our code.

Open `tsconfig.json` and configure the following compiler options:

```json
{
    {
  "compilerOptions": {
    "target": "ES2026",
    "module": "commonjs",
    "jsx": "react",
    "declaration": true,
    "declarationMap": true,
    "sourceMap": true,
    "outDir": "./dist",
    "esModuleInterop": true,
    "forceConsistentCasingInFileNames": true,
    "allowSyntheticDefaultImports": true,
    "strict": true,
    "skipLibCheck": true
  }
}
}
```




**Understanding the important options:**

- `jsx: "react"`: Allows TypeScript to work with JSX syntax used in React components.
- `declaration: true`: Generates TypeScript declaration files (`.d.ts`).
- `declarationMap: true`: Generates source maps for declaration files.
- `sourceMap: true`: Generates source maps to help debug the original source code.
- `allowSyntheticDefaultImports: true`: Allows default imports from modules that do not explicitly provide a default export.
- `strict: true`: Enables strict type-checking rules.
- `outDir: "./dist"`: Specifies the output directory for TypeScript compilation.

## 8. Install React and Its Type Definitions

Next, install React and React DOM.

```bash
yarn add react react-dom
```

React is the JavaScript library we will use to build our user interfaces, while React DOM handles rendering React components into the browser's DOM.

Since we are using TypeScript, we also need the React DOM type definitions.

```bash
yarn add -D @types/react-dom
```

These type definitions help TypeScript understand React DOM APIs and provide type checking during development.

## 9. Install Webpack and Its Dependencies

We will use Webpack to bundle our application into a single JavaScript file that can be served to the browser.

Install Webpack and Webpack CLI:

```bash
yarn add -D webpack
yarn add -D webpack-cli
```

Next, install the Fork TS Checker Webpack Plugin.

```bash
yarn add -D fork-ts-checker-webpack-plugin
```

This plugin performs TypeScript type checking separately from the Webpack compilation process.

We also need Babel to transform our React and TypeScript code into JavaScript that browsers can understand.

Install Babel and its required presets:

```bash
yarn add -D @babel/core
yarn add -D @babel/preset-react
yarn add -D @babel/preset-typescript
```

Install the Babel loader, which allows Webpack to use Babel when processing our source files.

```bash
yarn add -D babel-loader
```

Finally, install the source map loader:

```bash
yarn add -D source-map-loader
```

This loader allows Webpack to process existing source maps from JavaScript dependencies, making debugging easier.

## 10. Configure the Client Package.json

Open the `package.json` file inside the `client` folder.

Add the following script under the `scripts` section:

```json
"scripts": {
    "frontend": "webpack --config webpack.config.js --watch"
}
```

The command performs the following tasks:

- `webpack`: Runs the Webpack bundler.
- `--config webpack.config.js`: Specifies the Webpack configuration file.
- `--watch`: Watches our source files and automatically rebuilds the application whenever changes are detected.

Next, add the Babel configuration at the end of the `package.json` file:

```json
"babel": {
    "presets": [
        "@babel/preset-react",
        "@babel/preset-typescript"
    ]
}
```

This configuration tells Babel to use the React preset to transform JSX syntax and the TypeScript preset to remove TypeScript-specific syntax during compilation.

## 11. Create the Webpack Configuration File

Inside the `client` folder, create a file called `webpack.config.js`.

```bash
touch webpack.config.js
```

This file will contain the configuration Webpack needs to bundle our React application, including the entry point, output location, loaders, plugins, and source map settings.

## 12. Configure Webpack

Now that we have created `webpack.config.js`, open the file and add the following configuration:

```javascript
const webpack = require('webpack');
const path = require('path');
const ForkTsCheckerWebpackPlugin = require('fork-ts-checker-webpack-plugin');

module.exports = (env) => {
  const isProd = !!env && !!env.production;

  return {
    mode: isProd ? 'production' : 'development',
    entry: {
      spa: path.join(__dirname, 'index.tsx'),
    },
    target: 'web',
    resolve: {
      extensions: ['.ts', '.tsx', '.js'],
      fallback: {},
    },
    devtool: isProd ? undefined : 'source-map',
    module: {
      rules: [
        {
          test: /\.tsx?$/,
          use: [
            {
              loader: 'babel-loader',
            },
          ],
          exclude: /node_modules/,
        },
        {
          enforce: 'pre',
          test: /\.js$/,
          loader: 'source-map-loader',
        },
      ],
    },
    watchOptions: {
      ignored: [path.resolve(__dirname, 'node_modules')],
    },
    output: {
      filename: isProd
        ? '[name].bundle.[contenthash].min.js'
        : '[name].bundle.js',
      chunkFilename: isProd
        ? '[name].chunk.[contenthash].min.js'
        : '[name].chunk.js',
      path: path.resolve(__dirname, '../server'),
      publicPath: '/',
      libraryTarget: 'var',
      library: 'spa',
    },
    optimization: {
      minimize: isProd,
      minimizer: [],
      usedExports: true,
    },
    plugins: [
      new ForkTsCheckerWebpackPlugin(),
      new webpack.ProvidePlugin({
        Buffer: ['buffer', 'Buffer'],
      }),
      new webpack.ProvidePlugin({
        process: 'process/browser',
      }),
    ]
  }
}
```

### Understanding the Webpack Configuration

The Webpack configuration tells Webpack how to process, bundle, and generate our React application.

Here are some of the important configurations:

- **Entry:** Specifies `index.tsx` as the starting point of our React application.
- **Mode:** Determines whether Webpack runs in development or production mode.
- **Resolve:** Allows us to import TypeScript and JavaScript files without specifying their extensions.
- **Devtool:** Generates source maps in development mode to make debugging easier.
- **Module Rules:** Specifies how different files should be processed. We use `babel-loader` to transform TypeScript and JSX files and `source-map-loader` to process existing JavaScript source maps.
- **WatchOptions:** Prevents Webpack from monitoring the `node_modules` directory.
- **Output:** Specifies where the bundled application will be generated. In our case, the output goes directly into the `server` folder.
- **Plugins:** Adds additional functionality, including TypeScript type checking and automatic provision of `Buffer` and `process` variables.

One particularly important configuration is:

```javascript
output: {
    path: path.resolve(__dirname, '../server'),
    library: 'spa',
    libraryTarget: 'var',
}
```

This tells Webpack to generate our application bundle inside the `server` folder and expose it as a global variable called `spa`.

This is why we can call `spa.main()` from the `index.html` file we created earlier.

Also, because our entry point is named `spa`, Webpack generates the following file in development mode:

```text
spa.bundle.js
```

This matches the JavaScript file referenced in our server's `index.html`.

### Important: Additional Dependencies

Our Webpack configuration uses `buffer` and `process/browser`. Install these packages in the client folder:

```bash
yarn add buffer process
```

### 13. How the Client and Server Work Together

At this point, our project has two separate responsibilities:

1. The **client** uses React, TypeScript, Babel, and Webpack to develop and bundle the application.
2. The **server** uses `http-server` to deliver the generated HTML and JavaScript files to the browser.

The workflow is illustrated below:

```text
        CLIENT
           |
           v
      index.tsx
           |
           v
     TypeScript / JSX
           |
           v
          Babel
           |
           v
         Webpack
           |
           v
     spa.bundle.js
           |
           v
        SERVER
           |
           v
       index.html
           |
           v
        Browser
           |
           v
      React Application
```

**Important:** Webpack generates `spa.bundle.js` inside the `server` folder, so the server can access and serve it directly.

In the next step, we will create the `index.tsx` file, which will serve as the entry point for our React application.

The index.tsx file is the entry point of our React application. It contains the code that initializes React and tells it where to display the application in the browser.

Step 1: Create the File


Make sure you are inside the client folder, then run the following command:

```bash
touch index.tsx
``

Step 2: Add the React Code


Open the newly created index.tsx file in your code editor and add the following code:
```typescript
import React from 'react';
import { createRoot } from 'react-dom/client';

export const main = () => {
  // Find the root element in the HTML document
  const rootElement = document.querySelector("#root");

  // Check whether the root element exists
  if (!rootElement) {
    alert("Cannot find root element!");
    return;
  }

  // Create a React root
  const root = createRoot(rootElement);

  // Render the React application
  root.render(
    <div>
      <h1>Welcome to Web Application Development!</h1>
      <p>
        Congratulations! Your React application is running successfully.
      </p>
    </div>
  );
};
```


Step 3: Understand the Code

Let's understand what each part of the code does.

1. Import React

```ts
import React from 'react';
``

This imports the React library, which allows us to create and work with React components and JSX.

2. Import createRoot
```ts
import { createRoot } from 'react-dom/client';
```

The createRoot function is used to create a React root. This root determines where React will render the application in the browser.

3. Define the main function
```ts
export const main = () => {
  // Application code goes here
};
```

The main function is the starting point of our React application. We use export to make the function accessible outside this file.

Remember, our Webpack configuration exposes the application using the name spa. This allows the server's HTML file to start the application by calling:

spa.main();


4. Find the root HTML element
```ts
const rootElement = document.querySelector("#root");
```

This statement searches the HTML document for an element with the ID root.

For example, our server's index.html file contains:
```ts
<div id="root"></div>
```

React will use this element as the container for displaying the application.

5. Check whether the root element exists
```ts
if (!rootElement) {
  alert("Cannot find root element!");
  return;
}
```

This checks whether the browser found the root element.

If the element does not exist, the browser displays an alert message and stops executing the function. This prevents React from trying to render the application into an element that cannot be found.

6. Create a React root
```ts
const root = createRoot(rootElement);
```

This creates a React root associated with the HTML element we found earlier.

7. Render the application
```ts
root.render(
  <div>
    <h1>Welcome to Web Application Development!</h1>
    <p>
      Congratulations! Your React application is running successfully.
    </p>
  </div>
);
```

The render() method tells React what to display inside the root element.

In this example, we are displaying a heading and a paragraph using JSX.

Step 4: Save Your File


Save the index.tsx file.

If your frontend Webpack process is already running with the --watch option, Webpack will automatically detect the changes and rebuild the JavaScript bundle.

Otherwise, start the frontend build process from the client folder:
```bash
yarn frontend
```

Step 5: View the Application in Your Browser


Ensure that your backend server is also running
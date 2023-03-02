# Radial Gauge Visualization v3 (by Fastloop)


#### Quickstart Dev Instructions

1.  **Install Dependecies.**

    Using yarn, install all dependencies

    ```
    yarn
    ```

2.  **Make changes to the source code**

    Run and watch it:

    ````
    yarn watch
    ````

    This will generate and save file to the `dist/radialgauge_v3.js` file. This is ready to go file for looker, but it has to be server from webserver. There are several ways. 

    Liudas did this:

    - in the new shell and in `dist` directory run `python -m http.server`, this will run static server on port `8000` and will server js file.

    - in the new shell run `ngrok http 8000`, this will create secure tunnel between you pc port `8000`. Ngrok will give you public https address where you can access your js from anywhere. And we need this because Looker will not load any http (insecure) content. You can get ngrok from https://ngrok.com/. There are many tools like this.

3.  **Compile your code**

    You need to compile your react code, let's run:

    ```
    yarn build
    ```

    Recommended: Webpack can detect changes and build automatically

    ```
    yarn start
    ```

    Your compiled code can be found in this repo.


**`dist/radialgauge_v3.js`**: This visualization's minified distribution file. Ready for production. Running `yarn start` or `yarn watch` regenerates this file as well.

**`radialgauge.js`**: Old file, left for history. This visualization's minified distribution file.

**`radialgauge_v2.js`**: Old file, left for history. This visualization's minified distribution file.

**`LICENSE`**: Looker's Marketplace content License file.

**`manifest.lkml`**: Looker's external dependencies configuration file. The visualization object is defined here.

**`marketplace.json`**: A JSON file containing information the marketplace installer uses to set up this project.

**`/src`**: This directory will contain all of the visualization's source code.

**`/node_modules`**: The directory where all of the modules of code that your project depends on (npm packages) are automatically installed.

**`README.md`**: This! A text file containing useful reference information about this visualization.

**`yarn.lock`**: [Yarn](https://yarnpkg.com/) is a package manager alternative to npm. This file serves essentially the same purpose as `package-lock.json`, just for a different package management system.

**`.babelrc`**: A configuration file for the Babel jsx -> js compiler.

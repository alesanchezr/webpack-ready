# Using Webpack for the first time

This repository is an idea scenario to start working with webpack in 5 minutes.

It comes with an template structure of folders and files for any project that uses: HTML + JS + CSS3 + SASS

## Step by Step

1. Clone this repository as a template and get inside the project
```
$ git clone git@github.com:alesanchezr/webpack-ready.git
$ cd webpack-ready
```

Run npm install to download all the dependency libraries
```
$ npm install
```

Change the remote to you repository
```
$ git remote set-url origin <your repository url here>
```

Create your first bundle
```
$ npm run transpile-dev
```

Check that a public/bundle.js file has been created by Webpack. Read the output from the console that must be similar to this:

```sh
> workspace@1.0.0 transpile-dev /home/ubuntu/workspace
> webpack --config webpack.config.js

Hash: 64f06c46f625967b3aeb
Version: webpack 3.8.1
Time: 99ms
    Asset     Size  Chunks             Chunk Names
bundle.js  2.52 kB       0  [emitted]  main
   [0] ./src/app.js 51 bytes {0} [built]
```

### NOTE: You have to re-bundle every time yo update your JS or CSS/SASS files.

You are ready to go! You can commit & push to your new repository whenever you want.

## How to continue?

The application flow starts at **app.js**, you have to import any other files or assets into app.js in order for webpack to include them in the bundle.

For example, inside app.js you can do:

```js

    //This will include file.js into your bundle.
    import 'js/file2.js';
    
    //this will include the styles at index.scss to your bundle.
    require('../styles/index.scss');

```

1. All your JS and CSS code must go inside the src/ directory, and webpack will automaticly bundle them and export them into the public folder.
2. The HTML code must be inside public/index.html
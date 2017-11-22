# Using Webpack for the first time

1. Clone this repository as a template
```
$ git clone git@github.com:alesanchezr/webpack-ready.git
```

Run npm install to download all the dependency libraries
```
$ npm install
```

Change the remote to you repository
```
$ git remote set-url origin <your repository url here>
```

You are ready to go!

## How to continue?

Every time you want to transpile again (create a bundle) you have to do

```
$ npm run transpile-dev
```

The application flow starts at **app.js**, you have to import any other files or assets into app in order for webpack to include them in the bundle.

For example, inside app.js you can do:

```js

    //This will include file.js into your bundle.
    import 'js/file2';
    
    //this will include the styles at index.scss to your bundle.
    require('../styles/index.scss');

```

All your code must go inside the src folder, and webpack will automaticly bundle them and export them into the public folder.

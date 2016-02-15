# JavaScript code codex-js-checker

We want to use [JS Hint](http://jshint.com/) to detect errors and potential problems (to make our code run properly), and [JSCS](http://jscs.info/) to enforce a style guide (to make our code more readable).

We also want these two things to happen automagically, and run whenever we update our code.

There are two ways we can do this.

## Option 1: Easy - install for each project

Copy the `package.json` to your project.

Run `npm install`.

Now run `npm run checker` to have your JavaScript files watched for changes and checked for errors and readability. To stop the checker, hit `Ctrl + C`.

## Option 2: Advanced - install globally

Add the pacakges we need to your global npm like this:  `npm install -g jshint jscs chokidar`.

To have your JavaScript files watched  for changes and checked for errors and readability, run: `chokidar '*.js' -c 'jshint *.js && jscs --preset=grunt *.js'`. To stop the checker, hit `Ctrl + C`.

We're using the `grunt` preset for jscs because it matches a lot of the things we care about. Have a look at [the other JSCS presets](http://jscs.info/overview#presets) for more info.

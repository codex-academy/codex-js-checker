# JavaScript code codex-js-checker

We want to use [JS Hint](http://jshint.com/) to detect errors and potential problems (to make our code run properly), and [JSCS](http://jscs.info/) to enforce a style guide (to make our code more readable).

![](code-checker.jpg)

We would also like these two things to happen automagically, and run whenever we save our code. The checker will tell us which line number of our code it found the problem, and what it thinks the problem is. We can do this, and see the results on the command line.

## Option 1: Easy - install for each project

Copy the `package.json` to your project.

Run `npm install`.

Now run

```
npm run check
```

to (run the "check" script and) have your JavaScript files watched for changes and checked for errors and readability. To stop the checker, hit `Ctrl + C`.

## Option 2: Medium - install globally, run for each file

Add the packages we need to your global npm like this:

```
npm install -g jshint jscs chokidar
```

You can check for errors in a file called `index.js` by running:

```
jshint index.js
```

You can check for readability and style in a file called `app.js` by running:

```
jscs --preset=grunt app.js
```

You can check for errors **and** readability and style in a file called `fish.js` by running:

```
jshint fish.js && jscs --preset=grunt fish.js
```


## Option 3: Advanced - install globally, watch all files

Add the packages we need to your global npm like this:  `npm install -g jshint jscs chokidar`. Chokidar is a tiny app that watches files for changes.

To have all your JavaScript files watched for changes and checked for errors and readability, run:

```
chokidar '*.js' -c 'jshint *.js && jscs --preset=grunt *.js'
```

To stop the checker, hit `Ctrl + C`.

We're using the `grunt` preset for jscs because it matches a lot of the things we care about. Have a look at [the other JSCS presets](http://jscs.info/overview#presets) for more info.

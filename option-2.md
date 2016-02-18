# Option 2: Intermediate - install globally, run for each file

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

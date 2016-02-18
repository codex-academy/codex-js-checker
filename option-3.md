# Option 3: Advanced - install globally, watch all files

Add the packages we need to your global npm like this:  `npm install -g jshint jscs chokidar`. Chokidar is a tiny app that watches files for changes.

To have all your JavaScript files watched for changes and checked for errors and readability, run:

```
chokidar '*.js' -c 'jshint *.js && jscs --preset=grunt *.js'
```

To stop the checker, hit `Ctrl + C`.

We're using the `grunt` preset for jscs because it matches a lot of the things we care about. Have a look at [the other JSCS presets](http://jscs.info/overview#presets) for more info.

---
layout: default
---

# Option 1: install globally, run for each file

Add the packages we need to your global npm like this:

```
npm install -g jshint jscs
```

The `-g` means global, so you can run this command from anywhere.

## JS Hint

You can check for errors in a file called `index.js` by running:

```
jshint index.js
```

## JSCS

You can check for readability and style in a file called `app.js` by running:

```
jscs --preset=grunt app.js
```

## Combined!

You can check for errors **and** readability and style in a file called `fish.js` by running:

```
jshint fish.js && jscs --preset=grunt fish.js
```

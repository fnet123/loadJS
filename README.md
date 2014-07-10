loadJS
======

A simple function for asynchronously loading JavaScript files
[c]2014 @scottjehl, Filament Group, Inc.
Based on "Surefire Dom Insertion" http://goo.gl/REQGQ by Paul Irish
Licensed MIT

## Usage

Place the [`loadJS` function](https://github.com/filamentgroup/loadJS/blob/master/loadJS.js) inline in the `head` of your page (it can also be included in an external JavaScript file if preferable).

Then call it by passing it a stylesheet URL:

``` html
<head>
...
<script>
  loadJS( src ){ ... }
  // load a file
  loadJS( "path/to/script.js" );
</script>
...
</head>
```

## Limitations

`loadJS` is does nothing to manage execution order of requested scripts, so we do not advise using it to load multiple javascript files that depend on one another. It simply fetches a script and executes it as soon as possible. You can certainly use `loadJS` to load multiple scripts as long as those scripts are designed to execute independently of any other scripts being loaded by `loadJS`. 

#### Contributions and bug fixes

Both are very much appreciated - especially bug fixes. As for contributions, the goals of this project are to keep things very simple and utilitarian, so if we don't accept a feature addition, it's not necessarily because it's a bad idea. It just may not meet the goals of the project. Thanks!

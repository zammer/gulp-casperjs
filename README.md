# gulp-casperjs-options
## Forked from original [gulp-casperjs](https://github.com/NullRefExcep/gulp-casperjs) with minor updates

A [gulp](https://github.com/gulpjs/gulp) plugin for running [CasperJS](https://github.com/n1k0/casperjs) scripts

## Install

```
npm install --save-dev gulp-casperjs-options
```

## Usages

To add logging output option:
```js
var casperJs = require('gulp-casperjs-options');
gulp.task('logTest', function (){
    gulp.src('test.js')
        .pipe(casperjs({
            xunit: 'log.xml'
        }));
});
```

```js
var casperJs = require('gulp-casperjs');
gulp.task('test', function () {
  gulp.src('Globs of test files')
    .pipe(casperJs()); //run casperjs test
});
```
To change the command (default: `test`) use parameter `command`:
```js
var casperJs = require('gulp-casperjs');
gulp.task('casperCmd', function () {
  gulp.src('test.js')
    .pipe(casperJs({command:''})); //run capserjs test.js
});
```
Command can be `array` or `string`.
If command has value which cast to `false`, this parameter will be ignored.

To hide output from CasperJS use parameter `outputLog`:
```js
var casperJs = require('gulp-casperjs');
gulp.task('casperCmd', function () {
  gulp.src('test.js')
    .pipe(casperJs({outputLog: false})); //CasperJS output not show
});
```
Default value is `true`
## LICENSE

The MIT License (MIT)

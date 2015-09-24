electron-pdf-js
===============

[![NPM version][npm-image]][npm-url]
[![Downloads][downloads-image]][downloads-url]


A command line tool to generate PDF from URL, HTML or Markdown files with [electron](http://electron.atom.io/).

This is a fork of the original [electron-pdf](https://github.com/fraserxu/electron-pdf) package to add in additional
options including enabling javascript to be executed, custom height/width of the rendering browser window, allowing
use of external insecure content i.e. scripts and images and inclusion of a debug mode.

Install
-------

```
npm install electron-pdf-js -g
```

Usage
-----

### Build PDF

```

  A command line tool to generate PDF from URL, HTML or Markdown files

  Options
    --help                     Show this help
    --version                  Current version of package
    -i | --input               String - The path to the HTML file or url
    -o | --output              String - The path of the output PDF
    -c | --css                 String - The path to custom CSS

    -h | --height              Integer - Height of the browser window in pixels
    -w | --width               Integer - Width of the browser window in pixels

    -d | --debug               Boolean - Whether to display the electron browser window for debugging.
                                 false - default

    -j | --javascript          Boolean - Whether to enable execution of javascript.
                                 true - default

    --insecureContent          Boolean - Whether to allow use of insecure content, i.e. external images/scripts
                                 true - default

    -b | --printBackground     Boolean - Whether to print CSS backgrounds.
                                 false - true
    -s | --printSelectionOnly  Boolean - Whether to print selection only
                                 false - default
    -l | --landscape           Boolean - true for landscape, false for portrait.
                                 false - default
    -m | --marginType          Integer - Specify the type of margins to use
                                 0 - default
                                 1 - none
                                 2 - minimum

  Usage
    $ electron-pdf <input> <output>
    $ electron-pdf <input> <output> -l

  Examples
    $ electron-pdf http://benwritesco.de ~/Desktop/test.pdf
    $ electron-pdf ./index.html ~/Desktop/index.pdf
    $ electron-pdf ./README.md ~/Desktop/README.pdf -l
    $ electron-pdf ./README.md ~/Desktop/README.pdf -l -c my-awesome-css.css

```

Inspired by [electron-mocha](https://github.com/jprichardson/electron-mocha)

### License

MIT

[npm-image]: https://img.shields.io/npm/v/electron-pdf-js.svg?style=flat-square
[npm-url]: https://npmjs.org/package/electron-pdf-js
[downloads-image]: http://img.shields.io/npm/dm/electron-pdf-js.svg?style=flat-square
[downloads-url]: https://npmjs.org/package/electron-pdf-js

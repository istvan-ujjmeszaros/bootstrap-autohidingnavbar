# Bootstrap Auto-Hiding Navbar [![Build Status](https://secure.travis-ci.org/istvan-ujjmeszaros/bootstrap-autohidingnavbar.png?branch=master)](https://travis-ci.org/istvan-ujjmeszaros/bootstrap-autohidingnavbar)
Bootstrap Auto-Hiding Navbar is an extension for Bootstrap's fixed navbar which hides the navbar while the page is scrolling downwards and shows it the other way. The plugin is able to show/hide the navbar programmatically as well.

##Demo

[http://www.virtuosoft.eu/code/bootstrap-autohidingnavbar/](http://www.virtuosoft.eu/code/bootstrap-autohidingnavbar/)

## Usage

1. Download the latest tag from the [releases page](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/releases) or get it via **bower**:

```shell
$ bower install bootstrap-autohidingnavbar
```

2. Include **jQuery** and **Bootstrap**:

```html
<link rel="stylesheet" href="//cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/3.1.1/css/bootstrap.min.css">
<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/3.1.1/js/bootstrap.min.js"></script>
```

3. Include plugin's code:

```html
<script src="dist/jquery.bootstrap-autohidingnavbar.min.js"></script>
```

4. Call the plugin:

```javascript
$(".navbar-fixed-top").autoHidingNavbar({
  // see next for specifications
});
```

## Specifications

### Initialization parameters object

When calling `$(".navbar-fixed-top").autoHidingNavbar()` you can pass a parameters object with zero or more of the following:

- `disableAutohide`, defaults to `false`, set this to `true` if you want to show/hide the navbar programmatically.
- `showOnUpscroll`, defaults to `'true'`, the navbar shows up when scrolling the page upwards (otherwise it shows only when scroll is on page's top).
- `showOnBottom`, defaults to `'true'`, the navbar shows up when scroll reaches the page's end.
- `hideOffset`, defaults to `'auto'`, hides the navbar after scrolling that much pixel. Auto means the navbar's height.
- `animationDuration`, defaults to `'200'`, is the duration of the show and hide animations in milliseconds.

### Methods

You can modify the behavior and aspect of the plugin by calling its methods, most of them accepts a `value`.

To call methods on the auto hiding instance, use the following syntax:

```javascript
$(selector).autoHidingNavbar(methodName, parameter);
```

Here are the available methods:

- `setDisableAutohide(value)` to change the `disableAutohide` parameter.
- `setShowOnUpscroll(value)` to change the `showOnUpscroll` parameter.
- `setShowOnBottom(value)` to change the `showOnBottom` parameter.
- `setHideOffset(value)` to change the `hideOffset` parameter.
- `setAnimationDuration(value)` to change the `animationDuration` parameter.
- `show()` to show the navbar programmatically.
- `hide()` to hide the navbar programmatically.
- `destroy()` destroys the plugin instance.


## Structure

The basic structure of the project is given in the following way:

```
├── demo/
│   └── index.html
├── dist/
│   ├── jquery.bootstrap-autohidingnavbar.js
│   └── jquery.bootstrap-autohidingnavbar.min.js
├── src/
│   └── jquery.bootstrap-autohidingnavbar.js
├── .editorconfig
├── .gitignore
├── .jshintrc
├── .travis.yml
├── bootstrap-autohidingnavbar.jquery.json
├── bower.json
├── Gruntfile.js
└── package.json
```

#### [demo/](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/tree/master/demo)

Contains a simple HTML file to demonstrate the plugin.

#### [dist/](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/tree/master/dist)

This is where the generated files are stored once Grunt runs.

#### [src/](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/tree/master/src)

Contains the source files.

#### [.editorconfig](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/tree/master/.editorconfig)

This file is for unifying the coding style for different editors and IDEs.

> Check [editorconfig.org](http://editorconfig.org) if you haven't heard about this project yet.

#### [.gitignore](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/tree/master/.gitignore)

List of files that we don't want Git to track.

> Check this [Git Ignoring Files Guide](https://help.github.com/articles/ignoring-files) for more details.

#### [.jshintrc](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/tree/master/.jshintrc)

List of rules used by JSHint to detect errors and potential problems in JavaScript.

> Check [jshint.com](http://jshint.com/about/) if you haven't heard about this project yet.

#### [.travis.yml](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/tree/master/.travis.yml)

Definitions for continous integration using Travis.

> Check [travis-ci.org](http://about.travis-ci.org/) if you haven't heard about this project yet.

#### [bootstrap-autohidingnavbar.jquery.json](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/tree/master/bootstrap-autohidingnavbar.jquery.json)

Package manifest file used to publish plugins in jQuery Plugin Registry.

> Check this [Package Manifest Guide](http://plugins.jquery.com/docs/package-manifest/) for more details.

#### [Gruntfile.js](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/tree/master/Gruntfile.js)

Contains all automated tasks using Grunt.

> Check [gruntjs.com](http://gruntjs.com) if you haven't heard about this project yet.

#### [package.json](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/tree/master/package.json)

Specify all dependencies loaded via Node.JS.

> Check [NPM](https://npmjs.org/doc/json.html) for more details.

## Building

To build and test the plugin, you need:

- [**NodeJS**](www.nodejs.org) with **npm**
- **bower** (install it with `npm install bower --g`)
- **grunt-cli** (install it with `npm install grunt-cli --g`)

Then, `cd` to the project directory and install the required dependencies:

```shell
$ npm install
$ bower install
```

To run jshint on the plugin code, call:

```shell
$ grunt jshint
```

To build the output js and css files, with the related minified ones, run:

```shell
$ grunt
```

## Issues and Contributions

You can report any issue you may encounter on the [GitHub Issue Tracker](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/issues).

To contribute, please follow the [contribution guidelines](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/blob/master/CONTRIBUTING.md).

## History

Check [Release](https://github.com/istvan-ujjmeszaros/bootstrap-autohidingnavbar/releases) list.

## License

```
  Copyright 2014 István Ujj-Mészáros

  Licensed under the Apache License, Version 2.0 (the "License");
  you may not use this file except in compliance with the License.
  You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

  Unless required by applicable law or agreed to in writing, software
  distributed under the License is distributed on an "AS IS" BASIS,
  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  See the License for the specific language governing permissions and
  limitations under the License.
```

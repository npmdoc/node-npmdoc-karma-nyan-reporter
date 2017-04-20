# npmdoc-karma-nyan-reporter

#### api documentation for  karma-nyan-reporter (v0.2.5)  [![npm package](https://img.shields.io/npm/v/npmdoc-karma-nyan-reporter.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-karma-nyan-reporter) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-karma-nyan-reporter.svg)](https://travis-ci.org/npmdoc/node-npmdoc-karma-nyan-reporter)

#### Karma reporter with Nyan Cat style logging.

[![NPM](https://nodei.co/npm/karma-nyan-reporter.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/karma-nyan-reporter)

- [https://npmdoc.github.io/node-npmdoc-karma-nyan-reporter/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-karma-nyan-reporter/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-karma-nyan-reporter/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-karma-nyan-reporter/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-karma-nyan-reporter/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-karma-nyan-reporter/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": "Daniel Arlitt <dgarlitt@yahoo.com>",
    "bugs": {
        "url": "https://github.com/dgarlitt/karma-nyan-reporter/issues"
    },
    "dependencies": {
        "cli-color": "^0.3.2"
    },
    "description": "Karma reporter with Nyan Cat style logging.",
    "devDependencies": {
        "chai": "^2.3.0",
        "coveralls": "^2.11.2",
        "istanbul": "^0.3.15",
        "mocha": "^2.2.4",
        "mocha-lcov-reporter": "0.0.2",
        "rewire": "^2.3.3",
        "sinon": "^1.14.1",
        "sinon-chai": "^2.7.0"
    },
    "keywords": [
        "karma-plugin",
        "karma-reporter",
        "nyan",
        "cat"
    ],
    "license": "The MIT License (MIT)",
    "main": "index.js",
    "maintainers": [
        {
            "name": "Daniel Arlitt"
        }
    ],
    "name": "karma-nyan-reporter",
    "peerDependencies": {
        "karma": ">=0.9"
    },
    "repository": {
        "type": "git",
        "url": "https://github.com/dgarlitt/karma-nyan-reporter.git"
    },
    "scripts": {
        "coverage": "./node_modules/istanbul/lib/cli.js cover ./node_modules/mocha/bin/_mocha",
        "test": "./node_modules/mocha/bin/mocha -R spec ./test/*",
        "test-travis": "./node_modules/istanbul/lib/cli.js cover ./node_modules/mocha/bin/_mocha --report lcovonly -- -R spec  ./test/*"
    },
    "version": "0.2.5"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

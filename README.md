# api documentation for  [karma-nyan-reporter (v0.2.5)](https://github.com/dgarlitt/karma-nyan-reporter#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-karma-nyan-reporter.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-karma-nyan-reporter) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-karma-nyan-reporter.svg)](https://travis-ci.org/npmdoc/node-npmdoc-karma-nyan-reporter)
#### Karma reporter with Nyan Cat style logging.

[![NPM](https://nodei.co/npm/karma-nyan-reporter.png?downloads=true)](https://www.npmjs.com/package/karma-nyan-reporter)

[![apidoc](https://npmdoc.github.io/node-npmdoc-karma-nyan-reporter/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-karma-nyan-reporter_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-karma-nyan-reporter/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-karma-nyan-reporter/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-karma-nyan-reporter/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Daniel Arlitt",
        "email": "dgarlitt@yahoo.com"
    },
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
    "directories": {},
    "dist": {
        "shasum": "aab7925f34166ebcef9308bbee11679f58ddaa31",
        "tarball": "https://registry.npmjs.org/karma-nyan-reporter/-/karma-nyan-reporter-0.2.5.tgz"
    },
    "gitHead": "68da8261defe424c4ecf7805034f2de778c06d96",
    "homepage": "https://github.com/dgarlitt/karma-nyan-reporter#readme",
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
            "name": "dgarlitt",
            "email": "dgarlitt@yahoo.com"
        }
    ],
    "name": "karma-nyan-reporter",
    "optionalDependencies": {},
    "peerDependencies": {
        "karma": ">=0.9"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/dgarlitt/karma-nyan-reporter.git"
    },
    "scripts": {
        "coverage": "./node_modules/istanbul/lib/cli.js cover ./node_modules/mocha/bin/_mocha",
        "test": "./node_modules/mocha/bin/mocha -R spec ./test/*",
        "test-travis": "./node_modules/istanbul/lib/cli.js cover ./node_modules/mocha/bin/_mocha --report lcovonly -- -R spec  ./test/*"
    },
    "version": "0.2.5"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module karma-nyan-reporter](#apidoc.module.karma-nyan-reporter)
1.  object <span class="apidocSignatureSpan">karma-nyan-reporter.</span>nyanCat

#### [module karma-nyan-reporter.nyanCat](#apidoc.module.karma-nyan-reporter.nyanCat)
1.  [function <span class="apidocSignatureSpan">karma-nyan-reporter.nyanCat.</span>NyanCat (baseReporterDecorator, formatError, config)](#apidoc.element.karma-nyan-reporter.nyanCat.NyanCat)



# <a name="apidoc.module.karma-nyan-reporter"></a>[module karma-nyan-reporter](#apidoc.module.karma-nyan-reporter)



# <a name="apidoc.module.karma-nyan-reporter.nyanCat"></a>[module karma-nyan-reporter.nyanCat](#apidoc.module.karma-nyan-reporter.nyanCat)

#### <a name="apidoc.element.karma-nyan-reporter.nyanCat.NyanCat"></a>[function <span class="apidocSignatureSpan">karma-nyan-reporter.nyanCat.</span>NyanCat (baseReporterDecorator, formatError, config)](#apidoc.element.karma-nyan-reporter.nyanCat.NyanCat)
- description and source-code
```javascript
function NyanCat(baseReporterDecorator, formatError, config) {
  var self = this;
  var defaultOptions = function() {
    return {
      suppressErrorReport: false,
      suppressErrorHighlighting: false,
      numberOfRainbowLines: 4,
      renderOnRunCompleteOnly: false
    };
  };

  self.options = defaultOptions();

  if (config && config.nyanReporter) {
    // merge defaults
    Object.keys(self.options).forEach(function(optionName){
      if (config.nyanReporter.hasOwnProperty(optionName)) {
        self.options[optionName] = config.nyanReporter[optionName];
      }
    });
  }

  self.adapters = [fs.writeSync.bind(fs.writeSync, 1)];
  dataTypes.setErrorFormatterMethod(formatError);

  if (self.options.suppressErrorHighlighting) {
    dataTypes.suppressErrorHighlighting();
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

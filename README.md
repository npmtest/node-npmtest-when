# test coverage for  [when (v3.7.8)](http://cujojs.com)  [![npm package](https://img.shields.io/npm/v/npmtest-when.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-when) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-when.svg)](https://travis-ci.org/npmtest/node-npmtest-when)
#### A lightweight Promises/A+ and when() implementation, plus other async goodies.

[![NPM](https://nodei.co/npm/when.png?downloads=true)](https://www.npmjs.com/package/when)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-when/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-when/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-when/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-when/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-when/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-when/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-when/tree/gh-pages/build)|

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-when/build/screenCapture.buildCustomOrg.browser.coverage.html.png)](https://npmtest.github.io/node-npmtest-when/build/coverage.html/index.html)

[![test-report](https://npmtest.github.io/node-npmtest-when/build/screenCapture.buildCustomOrg.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmtest%252Fnode-npmtest-when%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-when/build/test-report.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-when/build/screenCapture.buildApidoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-when%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-when/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-when/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-when/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "browser": {
        "when": "./dist/browser/when.js",
        "vertx": false
    },
    "bugs": {
        "url": "https://github.com/cujojs/when/issues"
    },
    "contributors": [
        {
            "name": "Brian Cavalier",
            "url": "http://hovercraftstudios.com"
        },
        {
            "name": "John Hann",
            "url": "http://unscriptable.com"
        },
        {
            "name": "Scott Andrews"
        }
    ],
    "dependencies": {},
    "description": "A lightweight Promises/A+ and when() implementation, plus other async goodies.",
    "devDependencies": {
        "benchmark": "~1",
        "browserify": "~2",
        "buster": "~0.7",
        "exorcist": "~0.4",
        "glob": "^7.1.1",
        "jshint": "~2",
        "json5": "~0.2",
        "microtime": "~2",
        "mkdirp": "^0.5.1",
        "optimist": "~0.6",
        "poly": "^0.6.1",
        "promises-aplus-tests": "~2",
        "rest": "1.1.x",
        "sauce-connect-launcher": "~0.4",
        "uglify-js": "~2",
        "wd": "~0.2"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "c7130b6a7ea04693e842cdc9e7a1f2aa39a39f82",
        "tarball": "https://registry.npmjs.org/when/-/when-3.7.8.tgz"
    },
    "ender": {
        "files": [
            "*.js",
            "lib/*.js",
            "node/*.js",
            "unfold/*.js",
            "monitor/*.js",
            "lib/decorators/*.js"
        ]
    },
    "gitHead": "5c0a9ebaaf9bc859e76bd9584a9c9677e1e18f08",
    "homepage": "http://cujojs.com",
    "keywords": [
        "cujo",
        "Promises/A+",
        "promises-aplus",
        "promise",
        "promises",
        "deferred",
        "deferreds",
        "when",
        "async",
        "asynchronous",
        "ender"
    ],
    "license": "MIT",
    "main": "when.js",
    "maintainers": [
        {
            "name": "cujojs",
            "email": "info@cujojs.com"
        }
    ],
    "name": "when",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/cujojs/when.git"
    },
    "scripts": {
        "benchmark": "node benchmark/promise && node benchmark/map",
        "browser-test": "npm run build-browser-test && buster-static -e browser -p 8080",
        "browserify": "npm run browserify-es6 && npm run browserify-when && npm run browserify-debug",
        "browserify-debug": "node scripts/browserify.js debug",
        "browserify-es6": "node scripts/browserify.js es6",
        "browserify-when": "node scripts/browserify.js when",
        "build-browser-test": "browserify ./node_modules/poly/es5.js -o test/browser/es5.js && node scripts/browserify-tests",
        "ci": "npm test && node test/sauce.js",
        "prepublish": "npm run browserify && npm run uglify",
        "preversion": "npm run browserify && npm run uglify",
        "start": "buster-static -e browser",
        "test": "jshint . && buster-test -e node && promises-aplus-tests test/promises-aplus-adapter.js",
        "tunnel": "node test/sauce.js -m",
        "uglify": "npm run uglify-es6 && npm run uglify-when",
        "uglify-es6": "uglifyjs es6-shim/Promise.js --compress --mangle  --in-source-map es6-shim/Promise.js.map --source-map es6-shim/Promise.min.js.map -o es6-shim/Promise.min.js",
        "uglify-when": "uglifyjs dist/browser/when.js --compress --mangle  --in-source-map dist/browser/when.js.map --source-map dist/browser/when.min.js.map -o dist/browser/when.min.js"
    },
    "version": "3.7.8"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

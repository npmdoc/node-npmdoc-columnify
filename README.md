# npmdoc-columnify

#### basic api documentation for  [columnify (v1.5.4)](https://github.com/timoxley/columnify)  [![npm package](https://img.shields.io/npm/v/npmdoc-columnify.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-columnify) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-columnify.svg)](https://travis-ci.org/npmdoc/node-npmdoc-columnify)

#### Render data in text columns. Supports in-column text-wrap.

[![NPM](https://nodei.co/npm/columnify.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/columnify)

- [https://npmdoc.github.io/node-npmdoc-columnify/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-columnify/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-columnify/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-columnify/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-columnify/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-columnify/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tim Oxley"
    },
    "babel": {
        "presets": [
            "es2015"
        ]
    },
    "bugs": {
        "url": "https://github.com/timoxley/columnify/issues"
    },
    "dependencies": {
        "strip-ansi": "^3.0.0",
        "wcwidth": "^1.0.0"
    },
    "description": "Render data in text columns. Supports in-column text-wrap.",
    "devDependencies": {
        "babel": "^6.3.26",
        "babel-cli": "^6.3.17",
        "babel-preset-es2015": "^6.3.13",
        "chalk": "^1.1.1",
        "tap-spec": "^4.1.1",
        "tape": "^4.4.0"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "4737ddf1c7b69a8a7c340570782e947eec8e78bb",
        "tarball": "https://registry.npmjs.org/columnify/-/columnify-1.5.4.tgz"
    },
    "gitHead": "b5373b3d6344bf59e1ab63c912c188c34bce5889",
    "homepage": "https://github.com/timoxley/columnify",
    "keywords": [
        "column",
        "text",
        "ansi",
        "console",
        "terminal",
        "wrap",
        "table"
    ],
    "license": "MIT",
    "main": "columnify.js",
    "maintainers": [
        {
            "name": "timoxley"
        }
    ],
    "name": "columnify",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/timoxley/columnify.git"
    },
    "scripts": {
        "bench": "npm test && node bench",
        "prepublish": "make prepublish",
        "pretest": "npm prune",
        "test": "make prepublish && tape test/*.js | tap-spec"
    },
    "version": "1.5.4",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

# api documentation for  [columnify (v1.5.4)](https://github.com/timoxley/columnify)  [![npm package](https://img.shields.io/npm/v/npmdoc-columnify.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-columnify) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-columnify.svg)](https://travis-ci.org/npmdoc/node-npmdoc-columnify)
#### Render data in text columns. Supports in-column text-wrap.

[![NPM](https://nodei.co/npm/columnify.png?downloads=true)](https://www.npmjs.com/package/columnify)

[![apidoc](https://npmdoc.github.io/node-npmdoc-columnify/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-columnify_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-columnify/build/apidoc.html)

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
            "name": "timoxley",
            "email": "secoif@gmail.com"
        }
    ],
    "name": "columnify",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "1.5.4"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module columnify](#apidoc.module.columnify)
1.  object <span class="apidocSignatureSpan">columnify.</span>utils

#### [module columnify.utils](#apidoc.module.columnify.utils)
1.  [function <span class="apidocSignatureSpan">columnify.utils.</span>padCenter (str, max, chr)](#apidoc.element.columnify.utils.padCenter)
1.  [function <span class="apidocSignatureSpan">columnify.utils.</span>padLeft (str, max, chr)](#apidoc.element.columnify.utils.padLeft)
1.  [function <span class="apidocSignatureSpan">columnify.utils.</span>padRight (str, max, chr)](#apidoc.element.columnify.utils.padRight)
1.  [function <span class="apidocSignatureSpan">columnify.utils.</span>splitIntoLines (str, max)](#apidoc.element.columnify.utils.splitIntoLines)
1.  [function <span class="apidocSignatureSpan">columnify.utils.</span>splitLongWords (str, max, truncationChar)](#apidoc.element.columnify.utils.splitLongWords)
1.  [function <span class="apidocSignatureSpan">columnify.utils.</span>truncateString (str, max)](#apidoc.element.columnify.utils.truncateString)



# <a name="apidoc.module.columnify"></a>[module columnify](#apidoc.module.columnify)



# <a name="apidoc.module.columnify.utils"></a>[module columnify.utils](#apidoc.module.columnify.utils)

#### <a name="apidoc.element.columnify.utils.padCenter"></a>[function <span class="apidocSignatureSpan">columnify.utils.</span>padCenter (str, max, chr)](#apidoc.element.columnify.utils.padCenter)
- description and source-code
```javascript
function padCenter(str, max, chr) {
  str = str != null ? str : ''
  str = String(str)
  var length = max - wcwidth(str)
  if (length <= 0) return str
  var lengthLeft = Math.floor(length/2)
  var lengthRight = length - lengthLeft
  return repeatString(chr || ' ', lengthLeft) + str + repeatString(chr || ' ', lengthRight)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.columnify.utils.padLeft"></a>[function <span class="apidocSignatureSpan">columnify.utils.</span>padLeft (str, max, chr)](#apidoc.element.columnify.utils.padLeft)
- description and source-code
```javascript
function padLeft(str, max, chr) {
  str = str != null ? str : ''
  str = String(str)
  var length = max - wcwidth(str)
  if (length <= 0) return str
  return repeatString(chr || ' ', length) + str
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.columnify.utils.padRight"></a>[function <span class="apidocSignatureSpan">columnify.utils.</span>padRight (str, max, chr)](#apidoc.element.columnify.utils.padRight)
- description and source-code
```javascript
function padRight(str, max, chr) {
  str = str != null ? str : ''
  str = String(str)
  var length = max - wcwidth(str)
  if (length <= 0) return str
  return str + repeatString(chr || ' ', length)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.columnify.utils.splitIntoLines"></a>[function <span class="apidocSignatureSpan">columnify.utils.</span>splitIntoLines (str, max)](#apidoc.element.columnify.utils.splitIntoLines)
- description and source-code
```javascript
function splitIntoLines(str, max) {
  function _splitIntoLines(str, max) {
    return str.trim().split(' ').reduce(function(lines, word) {
      var line = lines[lines.length - 1]
      if (line && wcwidth(line.join(' ')) + wcwidth(word) < max) {
        lines[lines.length - 1].push(word) // add to line
      }
      else lines.push([word]) // new line
      return lines
    }, []).map(function(l) {
      return l.join(' ')
    })
  }
  return str.split('\n').map(function(str) {
    return _splitIntoLines(str, max)
  }).reduce(function(lines, line) {
    return lines.concat(line)
  }, [])
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.columnify.utils.splitLongWords"></a>[function <span class="apidocSignatureSpan">columnify.utils.</span>splitLongWords (str, max, truncationChar)](#apidoc.element.columnify.utils.splitLongWords)
- description and source-code
```javascript
function splitLongWords(str, max, truncationChar) {
  str = str.trim()
  var result = []
  var words = str.split(' ')
  var remainder = ''

  var truncationWidth = wcwidth(truncationChar)

  while (remainder || words.length) {
    if (remainder) {
      var word = remainder
      remainder = ''
    } else {
      var word = words.shift()
    }

    if (wcwidth(word) > max) {
      // slice is based on length no wcwidth
      var i = 0
      var wwidth = 0
      var limit = max - truncationWidth
      while (i < word.length) {
        var w = wcwidth(word.charAt(i))
        if (w + wwidth > limit) {
          break
        }
        wwidth += w
        ++i
      }

      remainder = word.slice(i) // get remainder
      // save remainder for next loop

      word = word.slice(0, i) // grab truncated word
      word += truncationChar // add trailing … or whatever
    }
    result.push(word)
  }

  return result.join(' ')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.columnify.utils.truncateString"></a>[function <span class="apidocSignatureSpan">columnify.utils.</span>truncateString (str, max)](#apidoc.element.columnify.utils.truncateString)
- description and source-code
```javascript
function truncateString(str, max) {

  str = str != null ? str : ''
  str = String(str)

  if(max == Infinity) return str

  var i = 0
  var wwidth = 0
  while (i < str.length) {
    var w = wcwidth(str.charAt(i))
    if(w + wwidth > max)
      break
    wwidth += w
    ++i
  }
  return str.slice(0, i)
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

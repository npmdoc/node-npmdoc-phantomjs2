# api documentation for  [phantomjs2 (v2.2.0)](https://github.com/zeevl/phantomjs2)  [![npm package](https://img.shields.io/npm/v/npmdoc-phantomjs2.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-phantomjs2) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-phantomjs2.svg)](https://travis-ci.org/npmdoc/node-npmdoc-phantomjs2)
#### Headless WebKit with JS API

[![NPM](https://nodei.co/npm/phantomjs2.png?downloads=true)](https://www.npmjs.com/package/phantomjs2)

[![apidoc](https://npmdoc.github.io/node-npmdoc-phantomjs2/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-phantomjs2_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-phantomjs2/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-phantomjs2/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-phantomjs2/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Steve Lamb",
        "email": "steve@stevelamb.io"
    },
    "bin": {
        "phantomjs": "./bin/phantomjs"
    },
    "bugs": {
        "url": "https://github.com/zeevl/phantomjs2/issues"
    },
    "dependencies": {
        "adm-zip": "0.4.4",
        "fs-extra": "~0.23.1",
        "glob": "^6.0.1",
        "kew": "0.4.0",
        "mkdirp": "^0.5.1",
        "npmconf": "2.1.1",
        "progress": "1.1.8",
        "request": "2.42.0",
        "request-progress": "0.3.1",
        "which": "~1.0.5"
    },
    "description": "Headless WebKit with JS API",
    "devDependencies": {
        "eslint": "1.5.1",
        "nodeunit": "0.9.0"
    },
    "directories": {},
    "dist": {
        "shasum": "75e3db02f913557a663055b0afb87998cf9160b3",
        "tarball": "https://registry.npmjs.org/phantomjs2/-/phantomjs2-2.2.0.tgz"
    },
    "gitHead": "baeef0416595fb39f147d4232c15c182f7f7526f",
    "homepage": "https://github.com/zeevl/phantomjs2",
    "keywords": [
        "phantomjs",
        "phantomjs2",
        "headless",
        "webkit"
    ],
    "license": "Apache-2.0",
    "main": "lib/phantomjs",
    "maintainers": [
        {
            "name": "zeevl",
            "email": "steve@stevelamb.io"
        }
    ],
    "name": "phantomjs2",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/zeevl/phantomjs2.git"
    },
    "scripts": {
        "install": "node install.js",
        "test": "nodeunit --reporter=minimal test/tests.js && eslint install.js"
    },
    "version": "2.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module phantomjs2](#apidoc.module.phantomjs2)
1.  [function <span class="apidocSignatureSpan">phantomjs2.</span>cleanPath (path)](#apidoc.element.phantomjs2.cleanPath)
1.  string <span class="apidocSignatureSpan">phantomjs2.</span>path
1.  string <span class="apidocSignatureSpan">phantomjs2.</span>version



# <a name="apidoc.module.phantomjs2"></a>[module phantomjs2](#apidoc.module.phantomjs2)

#### <a name="apidoc.element.phantomjs2.cleanPath"></a>[function <span class="apidocSignatureSpan">phantomjs2.</span>cleanPath (path)](#apidoc.element.phantomjs2.cleanPath)
- description and source-code
```javascript
cleanPath = function (path) {
  return path
      .replace(/:[^:]*node_modules[^:]*/g, '')
      .replace(/(^|:)\.\/bin(\:|$)/g, ':')
      .replace(/^:+/, '')
      .replace(/:+$/, '')
}
```
- example usage
```shell
...
    exit(1)
  }
})

// NPM adds bin directories to the path, which will cause 'which' to find the
// bin for this package not the actual phantomjs bin.  Also help out people who
// put ./bin on their path
process.env.PATH = helper.cleanPath(originalPath)

var libPath = path.join(__dirname, 'lib')
var pkgPath = path.join(libPath, 'phantom', 'bin')
var phantomPath = null
var tmpPath = null

var npmConfPromise = kew.nfcall(npmconf.load)
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

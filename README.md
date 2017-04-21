# npmtest-jwt-autorefresh

#### basic test coverage for  [jwt-autorefresh (v0.2.4)](http://jwt-autorefresh.js.org)  [![npm package](https://img.shields.io/npm/v/npmtest-jwt-autorefresh.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-jwt-autorefresh) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-jwt-autorefresh.svg)](https://travis-ci.org/npmtest/node-npmtest-jwt-autorefresh)

#### Factory to schedule and execute calls to refresh token endpoints in advance of token expiration.

[![NPM](https://nodei.co/npm/jwt-autorefresh.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/jwt-autorefresh)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-jwt-autorefresh/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-jwt-autorefresh/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-jwt-autorefresh/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/test-report.html](https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-jwt-autorefresh/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-jwt-autorefresh/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jwt-autorefresh/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jwt-autorefresh/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-jwt-autorefresh/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Cole Chamberlain",
        "url": "https://github.com/cchamberlain"
    },
    "bugs": {
        "url": "https://github.com/cchamberlain/jwt-autorefresh/issues"
    },
    "dependencies": {
        "bunyan": "^1.8.1",
        "chai": "^3.5.0",
        "jwt-simple": "^0.5.0",
        "npm-run-all": "^2.1.1"
    },
    "description": "Factory to schedule and execute calls to refresh token endpoints in advance of token expiration.",
    "devDependencies": {
        "babel-cli": "^6.7.7",
        "babel-preset-latest": "^6.6.0",
        "babel-preset-stage-2": "^6.5.0",
        "esdoc": "^0.4.6",
        "esdoc-es7-plugin": "0.0.3",
        "jest": "^16.0.1",
        "ncp": "^2.0.0",
        "npm-run-all": "^2.1.1",
        "rimraf": "^2.5.2"
    },
    "directories": {},
    "dist": {
        "shasum": "cf6ca15d827e4c65f8157b9ea53aeee04bc103ec",
        "tarball": "https://registry.npmjs.org/jwt-autorefresh/-/jwt-autorefresh-0.2.4.tgz"
    },
    "files": [
        "lib",
        "src",
        "doc"
    ],
    "gitHead": "1020272ff855d8a3119c08e11e00ab295bf2f3f9",
    "homepage": "http://jwt-autorefresh.js.org",
    "keywords": [
        "jwt",
        "refresh",
        "token",
        "openid",
        "oauth",
        "expiration",
        "exp",
        "keepalive",
        "unauthorized"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "cchamberlain"
        }
    ],
    "name": "jwt-autorefresh",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/cchamberlain/jwt-autorefresh.git"
    },
    "scripts": {
        "build": "babel src/lib -d lib --ignore __tests__,__mocks__",
        "clean": "rimraf lib doc",
        "doc": "esdoc -c ./esdoc.json && ncp CNAME doc/CNAME",
        "gh-pages-delete": "git branch -D gh-pages",
        "gh-pages-push": "git push -f origin gh-pages:gh-pages",
        "gh-pages-subtree": "git subtree split --prefix doc -b gh-pages",
        "git-save": "git add -A && git commit -am ",
        "postdoc": "npm run git-save -- doc",
        "postrelease": "npm run release-gh-pages",
        "postrelease-gh-pages": "npm run clean && npm run git-save -- clean && git push -u origin master --follow-tags",
        "prebuild": "npm run clean",
        "predoc": "rimraf doc",
        "prerelease": "run-p build test",
        "prerelease-gh-pages": "npm run doc",
        "release": "npm version patch && npm publish",
        "release-gh-pages": "run-s gh-pages-subtree gh-pages-push gh-pages-delete",
        "test": "jest"
    },
    "version": "0.2.4",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

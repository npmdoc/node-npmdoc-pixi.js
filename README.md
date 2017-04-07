# api documentation for  [pixi.js (v4.4.4)](http://goodboydigital.com/)  [![npm package](https://img.shields.io/npm/v/npmdoc-pixi.js.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-pixi.js) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-pixi.js.svg)](https://travis-ci.org/npmdoc/node-npmdoc-pixi.js)
#### Pixi.js is a fast lightweight 2D library that works across all devices.

[![NPM](https://nodei.co/npm/pixi.js.png?downloads=true)](https://www.npmjs.com/package/pixi.js)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pixi.js/build/screenCapture.buildNpmdoc.browser.%2Fhome%2Ftravis%2Fbuild%2Fnpmdoc%2Fnode-npmdoc-pixi.js%2Ftmp%2Fbuild%2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pixi.js/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-pixi.js/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-pixi.js/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Mat Groves"
    },
    "bugs": {
        "url": "https://github.com/pixijs/pixi.js/issues"
    },
    "contributors": [
        {
            "name": "Ivan Popelyshev",
            "email": "ivan.popelyshev@gmail.com"
        },
        {
            "name": "Matt Karl",
            "email": "matt@mattkarl.com"
        },
        {
            "name": "Chad Engler",
            "email": "chad@pantherdev.com"
        },
        {
            "name": "Richard Davey",
            "email": "rdavey@gmail.com"
        }
    ],
    "dependencies": {
        "bit-twiddle": "^1.0.2",
        "earcut": "^2.0.7",
        "eventemitter3": "^2.0.0",
        "ismobilejs": "^0.4.0",
        "object-assign": "^4.0.1",
        "pixi-gl-core": "^1.0.3",
        "resource-loader": "^2.0.6"
    },
    "description": "Pixi.js is a fast lightweight 2D library that works across all devices.",
    "devDependencies": {
        "babel-cli": "^6.18.0",
        "babel-plugin-static-fs": "^1.1.0",
        "babel-plugin-version-inline": "^1.0.0",
        "babel-preset-es2015": "^6.14.0",
        "babelify": "^7.3.0",
        "del": "^2.2.0",
        "electron": "^1.4.15",
        "eslint": "^3.5.0",
        "floss": "^2.0.1",
        "gh-pages": "^0.11.0",
        "jaguarjs-jsdoc": "^1.0.1",
        "js-md5": "^0.4.1",
        "jsdoc": "^3.4.2",
        "minimist": "^1.2.0",
        "mkdirp": "^0.5.1",
        "parallelshell": "^2.0.0",
        "pixify": "^1.7.0",
        "rimraf": "^2.5.3",
        "watch": "^0.19.1"
    },
    "directories": {},
    "dist": {
        "shasum": "cd260aff54140f6a259fc4bd2d00011ca0a928c4",
        "tarball": "https://registry.npmjs.org/pixi.js/-/pixi.js-4.4.4.tgz"
    },
    "files": [
        "dist/",
        "lib/",
        "CONTRIBUTING.md",
        "LICENSE",
        "package.json",
        "README.md"
    ],
    "gitHead": "eb952a92210840d5863d966836392f662da8ddb7",
    "homepage": "http://goodboydigital.com/",
    "license": "MIT",
    "main": "./lib/index.js",
    "maintainers": [
        {
            "name": "doormat23",
            "email": "mat@goodboydigital.com"
        },
        {
            "name": "englercj",
            "email": "englercj@live.com"
        }
    ],
    "name": "pixi.js",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/pixijs/pixi.js.git"
    },
    "scripts": {
        "build": "npm run dist",
        "clean": "rimraf dist lib && mkdirp dist && mkdir lib",
        "coverage": "npm test -- -c dist/pixi.js -s -h",
        "dist": "pixify -d dist -n PIXI -o pixi -t babelify",
        "docs": "jsdoc -c scripts/jsdoc.conf.json -R README.md",
        "lib": "babel src --out-dir lib -s",
        "lint": "eslint scripts src test --max-warnings 0",
        "lintfix": "npm run lint --fix",
        "postpublish": "node scripts/release.js",
        "postversion": "npm run clean && npm run build && npm run lib && npm test",
        "prebuild": "npm run lint",
        "precoverage": "rimraf coverage",
        "predist": "rimraf dist/**",
        "predocs": "rimraf docs/**",
        "prelib": "rimraf lib/**",
        "prerenders": "npm --prefix scripts/renders i scripts/renders",
        "prestart": "npm run clean",
        "publish:major": "npm version major --no-git-tag-version && npm publish",
        "publish:minor": "npm version minor --no-git-tag-version && npm publish",
        "publish:patch": "npm version patch --no-git-tag-version && npm publish",
        "renders": "electron scripts/renders",
        "start": "parallelshell \"npm run watch\" \"npm run watch:lint\" \"npm run watch:lib\"",
        "test": "floss --path test/index.js",
        "test:debug": "npm test -- --debug",
        "watch": "npm run dist -- --watch",
        "watch:lib": "npm run lib -- --watch",
        "watch:lint": "watch \"eslint scripts src test || exit 0\" src"
    },
    "version": "4.4.4"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module pixi.js](#apidoc.module.pixi.js)



# <a name="apidoc.module.pixi.js"></a>[module pixi.js](#apidoc.module.pixi.js)



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

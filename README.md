# npmdoc-pixi.js

#### api documentation for  [pixi.js (v4.5.1)](http://goodboydigital.com/)  [![npm package](https://img.shields.io/npm/v/npmdoc-pixi.js.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-pixi.js) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-pixi.js.svg)](https://travis-ci.org/npmdoc/node-npmdoc-pixi.js)

#### Pixi.js is a fast lightweight 2D library that works across all devices.

[![NPM](https://nodei.co/npm/pixi.js.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/pixi.js)

- [https://npmdoc.github.io/node-npmdoc-pixi.js/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-pixi.js/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pixi.js/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pixi.js/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-pixi.js/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-pixi.js/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "pixi.js",
    "version": "4.5.1",
    "description": "Pixi.js is a fast lightweight 2D library that works across all devices.",
    "author": "Mat Groves",
    "contributors": [
        "Ivan Popelyshev <ivan.popelyshev@gmail.com>",
        "Matt Karl <matt@mattkarl.com>",
        "Chad Engler <chad@pantherdev.com>",
        "Richard Davey <rdavey@gmail.com>"
    ],
    "main": "./lib/index.js",
    "homepage": "http://goodboydigital.com/",
    "bugs": "https://github.com/pixijs/pixi.js/issues",
    "license": "MIT",
    "repository": {
        "type": "git",
        "url": "https://github.com/pixijs/pixi.js.git"
    },
    "scripts": {
        "clean": "rimraf dist lib && mkdirp dist && mkdir lib",
        "prestart": "npm run clean",
        "start": "parallelshell \"npm run watch\" \"npm run watch:lint\" \"npm run watch:lib\"",
        "watch": "npm run dist -- --watch",
        "watch:lib": "npm run lib -- --watch",
        "watch:lint": "watch \"eslint scripts src test || exit 0\" src",
        "test": "floss --path test/index.js",
        "test:debug": "npm test -- --debug",
        "prerenders": "npm --prefix scripts/renders i scripts/renders",
        "renders": "electron scripts/renders",
        "precoverage": "rimraf coverage",
        "coverage": "npm test -- -c dist/pixi.js -s -h",
        "lint": "eslint scripts src test --max-warnings 0",
        "lintfix": "npm run lint --fix",
        "prebuild": "npm run lint",
        "build": "npm run dist",
        "predist": "rimraf dist/**",
        "dist": "pixify -d dist -n PIXI -o pixi -t babelify",
        "prelib": "rimraf lib/**",
        "lib": "babel src --out-dir lib -s",
        "predocs": "rimraf docs/**",
        "docs": "jsdoc -c scripts/jsdoc.conf.json -R README.md",
        "publish:patch": "npm version patch && npm publish",
        "publish:minor": "npm version minor && npm publish",
        "publish:major": "npm version major && npm publish",
        "postversion": "npm run clean && npm run build && npm run lib && npm test",
        "postpublish": "git push && git push --tags && npm run release",
        "release": "node scripts/release"
    },
    "files": [
        "dist/",
        "lib/",
        "CONTRIBUTING.md",
        "LICENSE",
        "package.json",
        "README.md"
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
        "gh-pages": "^0.12.0",
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
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

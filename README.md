# istanbul-coveralls 

[![npm version](https://badge.fury.io/js/%40toolisticon%2Fistanbul-coveralls.svg)](https://www.npmjs.com/package/@toolisticon/istanbul-coveralls)
[![Build Status](https://travis-ci.org/toolisticon/istanbul-coveralls.svg?branch=master)](https://travis-ci.org/toolisticon/istanbul-coveralls)
[![Coverage Status](https://img.shields.io/coveralls/toolisticon/istanbul-coveralls.svg)](https://coveralls.io/r/toolisticon/istanbul-coveralls?branch=master)
[![Dependency Status](https://david-dm.org/toolisticon/istanbul-coveralls.svg)](https://david-dm.org/toolisticon/istanbul-coveralls)
[![devDependency Status](https://david-dm.org/toolisticon/istanbul-coveralls/dev-status.svg)](https://david-dm.org/toolisticon/istanbul-coveralls#info=devDependencies) [![Greenkeeper badge](https://badges.greenkeeper.io/toolisticon/istanbul-coveralls.svg)](https://greenkeeper.io/)

A simple alias for [istanbul](https://github.com/gotwarlost/istanbul) + [node-coveralls](https://github.com/cainus/node-coveralls)

```sh
istanbul cover test.js && cat ./coverage/lcov.info | coveralls && rm -rf ./coverage
```

↓

```sh
istanbul cover test.js && istanbul-coveralls
```

## Installation

[Use npm](https://docs.npmjs.com/cli/install).

```sh
npm install --save-dev istanbul istanbul-coveralls
```

## Usage

1. Write a coverage information file under `./coverage` by using [`istanbul cover` command](https://github.com/gotwarlost/istanbul#the-cover-command) or [the API of istanbul](https://github.com/gotwarlost/istanbul#api).
2. Run `istanbul-coveralls` command. See [the docs of node-coveralls](https://github.com/cainus/node-coveralls#usage) for more information about its usage.

### Option

#### `--no-rm`

By default, it removes `./coverage` after coverage reporting. If `--no-rm` flag is enabled, it doesn't remove the directory.

```sh
istanbul cover test.js && istanbul-coveralls --no-rm
```

## Example

### [Mocha](http://mochajs.org/)

```sh
istanbul cover ./node_modules/.bin/_mocha && ./node_modules/.bin/istanbul-coveralls
```

If you run the test as a [npm script](https://docs.npmjs.com/misc/scripts), [you can omit directory names from the command](https://docs.npmjs.com/misc/scripts#path).

```sh
istanbul cover _mocha && istanbul-coveralls
```

## License

Copyright (c) 2018 [Holisticon AG](https://github.com/toolisticon)

Licensed under [the MIT LIcense](./LICENSE).

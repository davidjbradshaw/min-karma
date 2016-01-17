# min-karma [![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/) [![bitHound Dependencies](https://www.bithound.io/github/dmitriz/min-karma/badges/dependencies.svg)](https://www.bithound.io/github/dmitriz/min-karma/master/dependencies/npm) [![bitHound Code](https://www.bithound.io/github/dmitriz/min-karma/badges/code.svg)](https://www.bithound.io/github/dmitriz/min-karma) [![Code Climate](https://codeclimate.com/github/dmitriz/min-karma/badges/gpa.svg)](https://codeclimate.com/github/dmitriz/min-karma)
Minimal Karma runner *Setup* and [*Package*](https://www.npmjs.com/package/min-karma) &mdash; Start testing now!


## Karma
[Karma](http://karma-runner.github.io/0.13/index.html) is a JavaScript Test Runner, one of the most popular and friendliest for beginners.

> On the [AngularJS](https://angularjs.org/) team, we rely on testing and we always seek better tools to make our life easier. That's why we created
Karma - a test runner that fits all our needs.


## Why?
- Many setups are bloated with unnecessary options and packages.
- Start clean and minimal and extend as you go.
- Add single package to your project instead of many, to get your tests up and running.

## Use cases
- You have a project and want to add unit/integration/whatever tests &mdash; [install the package](#to-use-as-package-add-to-your-project).
- You want to quickly evaluate Karma runner and play with in a clean folder &mdash; [clone or download the repository](#to-use-as-separate-repository).

## Features
- Minimal functional Karma config file.
- Use as *repository* (`git clone`) or *package* (`npm install`).
- Installs all testing packages as dependencies, no need to install them manually.
- Automatically and gracefully (without overwriting) copied to your project directory:
  - Basic testing example in the `examples` folder.
  - Minimal functional configuration file `karma.conf.js`:

		```js
		module.exports = function (config) {
		  config.set({
		    frameworks: ['jasmine'],
		    files: [
		      'examples/**/*.js'
		    ],
		    browsers: ['Chrome']
		  })
		}
		```

## If you are new to Node
[Download and Install Node.js](https://nodejs.org/download/), see [How do I get started with Node.js](http://stackoverflow.com/questions/2353818/how-do-i-get-started-with-node-js) for more information.


## To use as separate Repository: 
### Clone
```sh
git clone https://github.com/dmitriz/min-karma
```
or simply [Download this Repository](https://github.com/dmitriz/min-karma/archive/master.zip),
unzip it and `cd min-karma-master`.

### Install dependencies
```sh
npm install --save-dev
```

## To use as Package (add to your project):
In your main project directory (should contain `package.json`):
```sh
npm install min-karma --save
```

## Getting started
Run your tests:
```sh
karma start
```
Now try to edit files inside `examples` folder and see how karma is watching and updating your test results.

## Basic testing example &mdash; inside `examples` folder
```js
// function to test
function add (a, b) {
	return a + b
}

// the test
describe('Addition', function () {
	it('should add numbers', function () {
		expect(add(2, 4)).toBe(6)
		expect(add(2, 4)).not.toBe(2)
	})
})
```

**Tip.** Keep your tests next to their testees for better [cohesion](https://en.wikipedia.org/wiki/Cohesion_(computer_science)). Avoid putting them into separate folders (like `tests`) away from your code.

Enjoy!

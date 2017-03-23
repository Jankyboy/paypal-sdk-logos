Grumbler
--------

https://medium.com/@bluepnume/introducing-grumbler-an-opinionated-javascript-module-template-612245e06d00

A template for writing distributable javascript modules.

Javascript libraries are fun to write. Setting up all of the boilerplate to get your build up and running is not so fun.

This module provides a forkable module template, which you can use to kick-start a new javascript library. Once you've done that, feel free to come back and switch out the tooling for whatever you prefer.

Features
--------

- Build minified and unminified versions of your code, with source maps
- Use ES2015 out of the box
- Write headless Karma / Mocha tests, which run in PhantomJS and other browsers, with code coverage reports
- Integrate with Travis CI out of the box
- Write error free, type-safe code with ESLint, Flow Type, and Flow-Runtime

Technologies
------------

- gulp
- babel
- eslint
- flowtype
- flow-runtime
- karma
- phantomjs
- mocha
- istanbul
- webpack
- npm
- travis

Quick Start
-----------

#### Getting Started

- Fork the module
- Run setup: `./setup.sh`
- Start editing code in `./src` and writing tests in `./tests`
- `gulp build`

#### Building

```bash
gulp build
```

#### Tests

- Edit tests in `./test/tests`
- Run the tests:

  ```bash
  gulp test
  ```

#### Testing with different/multiple browsers

```bash
gulp test --browser=PhantomJS
gulp test --browser=Chrome
gulp test --browser=Safari
gulp test --browser=Firefox
gulp test --browser=PhantomJS,Chrome,Safari,Firefox
```

#### Keeping the browser open after tests

```bash
gulp test --browser=Chrome --keep-browser-open
```

#### Publishing

##### Before you publish for the first time:

- Delete the example code in `./src`, `./test/tests` and `./demo`
- Edit the module name in `package.json`
- Edit `README.md` and `CONTRIBUTING.md`

##### Then:

- Publish your code: `./publish.sh`

FAQ
---

- **Who is this for?**
  - Anyone who wants to get started quickly on a javascript library without setting up a lot of boilerplate
  - Anyone who wants a fairly healthy opinionated set of defaults to get started with
  - Anyone new to writing front-end modules, who doesn't want to immediately research which modules to use to build their code

- **Who this is *not* for?**
  - Anyone who needs/wants tight control over their project, and which specific build tools they want to use

- **Why use technology X/Y/Z?**

  Probably because it's been a good fit for us in the past. We wanted our focus to be around (fairly) standardized
  javascript as much as possible, rather than compiled-to-javascript languages, hence the use of babel, flow, etc.

- **So you just took a bunch of build-tools and daisy-chained them together?**

  Yep, pretty much. This is not anything remotely technically impressive, or new, or innovative. It's just a healthy
  set of defaults to get started with if you're building a front-end distributable library.

- **Can I improve this template?**

  By all means, please feel to raise a PR, but if it's a big change, try to open an issue first so we can chat!
	
- **What about support for React, Ember, framework X or Y?**

  Wanted to keep this module as framework-agnostic as possible. Not to mention there are already pretty good boilerplates out there for whatever framework you're using, I'll bet. Otherwise please feel free to be my guest and fork `grumbler-superawesomeframework` if it's helpful.

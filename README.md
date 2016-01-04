Repro an apparent npm/node bug from https://github.com/pouchdb/pouchdb/pull/4741

Steps:

    npm install

Error (abridged):

```
> node-pre-gyp install --fallback-to-build

[fsevents] Success: "/private/tmp/testy/node_modules/fsevents/lib/binding/Release/node-v47-darwin-x64/fse.node" is installed via remote

> leveldown@1.4.2 install /private/tmp/testy/node_modules/pouchdb/node_modules/leveldown
> prebuild --download

module.js:328
    throw err;
    ^

Error: Cannot find module 'inherits'
    at Function.Module._resolveFilename (module.js:326:15)
    at Function.Module._load (module.js:277:25)
    at Module.require (module.js:354:17)
    at require (internal/module.js:12:17)
    at Object.<anonymous> (/private/tmp/testy/node_modules/are-we-there-yet/node_modules/readable-stream/lib/_stream_readable.js:45:17)
    at Module._compile (module.js:398:26)
    at Object.Module._extensions..js (module.js:405:10)
    at Module.load (module.js:344:32)
    at Function.Module._load (module.js:301:12)
    at Module.require (module.js:354:17)
npm WARN install:leveldown@1.4.2 leveldown@1.4.2 install: `prebuild --download`
npm WARN install:leveldown@1.4.2 Exit status 1

> phantomjs@1.9.19 install /private/tmp/testy/node_modules/phantomjs
> node install.js

module.js:328
    throw err;
    ^

Error: Cannot find module 'inherits'
    at Function.Module._resolveFilename (module.js:326:15)
    at Function.Module._load (module.js:277:25)
    at Module.require (module.js:354:17)
    at require (internal/module.js:12:17)
    at Object.<anonymous> (/private/tmp/testy/node_modules/rimraf/node_modules/glob/glob.js:46:16)
    at Module._compile (module.js:398:26)
    at Object.Module._extensions..js (module.js:405:10)
    at Module.load (module.js:344:32)
    at Function.Module._load (module.js:301:12)
    at Module.require (module.js:354:17)
```

# Primeng12 lib issues
## _Issue when adding primeng 12 module on a module library._

This project is a simple angular 12 project generate like this :
```sh
ng new primeng12libissues
cd primeng12libissues/
ng g library testlib
npm i primeng@12
```

Then I went to the module testlib.module.ts and added : ButtonModule.

## Reproduce error

```sh
npm run build:lib
```
You should get the following error :
```sh
> primeng12libissues@0.0.0 build:lib /Users/adrien/workspace/test/primeng12libissues
> ng-packagr -p projects/testlib/ng-package.json

Building Angular Package

------------------------------------------------------------------------------
Building entry point 'testlib'
------------------------------------------------------------------------------
✖ Compiling with Angular in legacy View Engine compilation mode.
Maximum call stack size exceeded
npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! primeng12libissues@0.0.0 build:lib: `ng-packagr -p projects/testlib/ng-package.json`
npm ERR! Exit status 1
npm ERR! 
npm ERR! Failed at the primeng12libissues@0.0.0 build:lib script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.
```

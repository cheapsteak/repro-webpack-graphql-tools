This repo reproduces an error when trying to use methods from graphql-tools in web bundles compiled by webpack 4


Install dependnecies (webpack and graphql-tools)
```bash
yarn 
```

Build the bundle
```bash
yarn build # builds the bundle 
```

Then open the file at page.html

You should see 

```
Uncaught ReferenceError: require is not defined
    at eval (instanceOf.mjs:34)
    at Object../node_modules/graphql/jsutils/instanceOf.mjs (bundle.js:886)
    at __webpack_require__ (bundle.js:20)
    at eval (definition.mjs:46)
    at Object../node_modules/graphql/type/definition.mjs (bundle.js:1210)
    at __webpack_require__ (bundle.js:20)
    at eval (validate.mjs:4)
    at Object../node_modules/graphql/type/validate.mjs (bundle.js:1282)
    at __webpack_require__ (bundle.js:20)
    at eval (graphql.mjs:4)
```


# Fresh sapper (0.27.16) project crashes on lodash import

`npm run dev` reports an error when [`./src/routes/_layout.svelte`](./src/routes/_layout.svelte#L3) (line 3) imports `lodash` or one of its functions. The error is:

```
var freeGlobal = typeof commonjsGlobal == 'object' && commonjsGlobal && commonjsHelpers.commonjsGlobal.Object === Object && commonjsGlobal;
                                                                        ^
ReferenceError: commonjsHelpers is not defined
    at /[some-path]/fresh-sapper-lodash-error/__sapper__/dev/server/server.js:790:75
```
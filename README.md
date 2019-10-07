# NgbPureGetters

Bundles with `ng build --prod`:
```
-rw-r--r--   1 ced-pro  staff  172713  7 oct 10:03 main-es2015.b0dd87f66a011315f351.js
-rw-r--r--   1 ced-pro  staff  204763  7 oct 10:03 main-es5.b0dd87f66a011315f351.js
-rw-r--r--   1 ced-pro  staff   37339  7 oct 10:03 polyfills-es2015.d25d15356b84b54fd47e.js
-rw-r--r--   1 ced-pro  staff  128097  7 oct 10:03 polyfills-es5.5ef177e03e3155ddaf9d.js
-rw-r--r--   1 ced-pro  staff    1485  7 oct 10:03 runtime-es2015.2c273926116239a40a8f.js
-rw-r--r--   1 ced-pro  staff    1485  7 oct 10:03 runtime-es5.2c273926116239a40a8f.js
```

Repro: edit webpack config, and remove the `pure_getters` option.

```
vim node_modules/@angular-devkit/build-angular/src/angular-cli-files/models/webpack-configs/common.js
# look for `pure_getters` and remove the line
# rebuild
ng build --prod
```

Budnles without `pure_getters`:
```
-rw-r--r--   1 ced-pro  staff  173195  7 oct 10:04 main-es2015.daf7f03c60c42b1c6405.js
-rw-r--r--   1 ced-pro  staff  205229  7 oct 10:04 main-es5.daf7f03c60c42b1c6405.js
-rw-r--r--   1 ced-pro  staff   37444  7 oct 10:04 polyfills-es2015.1717e9c58015c44cbb20.js
-rw-r--r--   1 ced-pro  staff  128241  7 oct 10:04 polyfills-es5.60dd8afa4320e59000eb.js
-rw-r--r--   1 ced-pro  staff    1494  7 oct 10:04 runtime-es2015.9a4265baeb59cced2497.js
-rw-r--r--   1 ced-pro  staff    1494  7 oct 10:04 runtime-es5.9a4265baeb59cced2497.js
```

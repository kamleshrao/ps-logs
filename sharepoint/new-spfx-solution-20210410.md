# Errors while creating New SharePoint SPFx Solution in Windows 10 

## My environment setup:
```
C:\Users\krnotes>ver

Microsoft Windows [Version 10.0.19041.867]

C:\Users\krnotes>node -v
v14.16.1

C:\Users\krnotes>npm -v
6.14.12

C:\Users\krnotes>npm list -g --depth=0
C:\Users\krnotes\AppData\Roaming\npm
+-- @microsoft/generator-sharepoint@1.11.0
+-- gulp@4.0.2
`-- yo@3.1.1
```


## Creating the HelloWorld WebPart by running the Yeoman SharePoint Generator.

``` 
Microsoft Windows [Version 10.0.19041.867]
(c) 2020 Microsoft Corporation. All rights reserved.

C:\Users\krnotes>node -v
v14.16.1

C:\Users\krnotes>npm -v
6.14.12

C:\Users\krnotes>npm install gulp yo @microsoft/generator-sharepoint --global
npm WARN deprecated urix@0.1.0: Please see https://github.com/lydell/urix#deprecated
npm WARN deprecated resolve-url@0.2.1: https://github.com/lydell/resolve-url#deprecated
npm WARN deprecated chokidar@2.1.8: Chokidar 2 will break on node v14+. Upgrade to chokidar 3 with 15x less dependencies.
npm WARN deprecated fsevents@1.2.13: fsevents 1 will break on node v14+ and could be using insecure binaries. Upgrade to fsevents 2.
npm WARN deprecated request@2.88.2: request has been deprecated, see https://github.com/request/request/issues/3142
npm WARN deprecated har-validator@5.1.5: this library is no longer supported
npm WARN deprecated cross-spawn-async@2.2.5: cross-spawn no longer requires a build toolchain, use it instead
C:\Users\krnotes\AppData\Roaming\npm\gulp -> C:\Users\krnotes\AppData\Roaming\npm\node_modules\gulp\bin\gulp.js
C:\Users\krnotes\AppData\Roaming\npm\yo -> C:\Users\krnotes\AppData\Roaming\npm\node_modules\yo\lib\cli.js
C:\Users\krnotes\AppData\Roaming\npm\yo-complete -> C:\Users\krnotes\AppData\Roaming\npm\node_modules\yo\lib\completion\index.js

> ejs@2.7.4 postinstall C:\Users\krnotes\AppData\Roaming\npm\node_modules\@microsoft\generator-sharepoint\node_modules\ejs
> node ./postinstall.js

Thank you for installing EJS: built with the Jake JavaScript build tool (https://jakejs.com/)


> core-js@3.10.1 postinstall C:\Users\krnotes\AppData\Roaming\npm\node_modules\yo\node_modules\core-js
> node -e "try{require('./postinstall')}catch(e){}"

Thank you for using core-js ( https://github.com/zloirock/core-js ) for polyfilling JavaScript standard library!

The project needs your help! Please consider supporting of core-js on Open Collective or Patreon:
> https://opencollective.com/core-js
> https://www.patreon.com/zloirock

Also, the author of core-js ( https://github.com/zloirock ) is looking for a good job -)


> ejs@2.7.4 postinstall C:\Users\krnotes\AppData\Roaming\npm\node_modules\yo\node_modules\ejs
> node ./postinstall.js

Thank you for installing EJS: built with the Jake JavaScript build tool (https://jakejs.com/)


> spawn-sync@1.0.15 postinstall C:\Users\krnotes\AppData\Roaming\npm\node_modules\yo\node_modules\spawn-sync
> node postinstall


> yo@3.1.1 postinstall C:\Users\krnotes\AppData\Roaming\npm\node_modules\yo
> yodoctor


Yeoman Doctor
Running sanity checks on your system

√ No .bowerrc file in home directory
√ Global configuration file is valid
√ NODE_PATH matches the npm root
√ No .yo-rc.json file in home directory
√ Node.js version
√ npm version
√ yo version

Everything looks all right!
npm WARN notsup Unsupported engine for got@5.7.1: wanted: {"node":">=0.10.0 <7"} (current: {"node":"14.16.1","npm":"6.14.12"})
npm WARN notsup Not compatible with your version of node/npm: got@5.7.1
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@^1.2.7 (node_modules\gulp\node_modules\chokidar\node_modules\fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@1.2.13: wanted {"os":"darwin","arch":"any"} (current: {"os":"win32","arch":"x64"})

+ yo@3.1.1
+ gulp@4.0.2
+ @microsoft/generator-sharepoint@1.11.0
added 1509 packages from 456 contributors in 110.135s

C:\Users\krnotes>d:

D:\>md code

D:\>cd code

D:\code>md md helloworld-webpart

D:\code>cd helloworld-webpart

D:\code\helloworld-webpart>yo @microsoft/sharepoint
? ==========================================================================
We're constantly looking for ways to make yo better!
May we anonymously report usage statistics to improve the tool over time?
More info: https://github.com/yeoman/insight & http://yeoman.io
========================================================================== No

     _-----_
    |       |    .--------------------------.
    |--(o)--|    |      Welcome to the      |
   `---------´   |  SharePoint Client-side  |
    ( _´U`_ )    |    Solution Generator    |
    /___A___\    '--------------------------'
     |  ~  |
   __'.___.'__
 ´   `  |° ´ Y `

Let's create a new SharePoint solution.
? What is your solution name? helloworld-webpart
? Which baseline packages do you want to target for your component(s)? SharePoint Online only (latest)
? Where do you want to place the files? Use the current folder
Found npm version 6.14.12
? Do you want to allow the tenant admin the choice of being able to deploy the solution to all sites immediately without
 running any feature deployment or adding apps in sites? No
? Will the components in the solution require permissions to access web APIs that are unique and not shared with other c
omponents in the tenant? No
? Which type of client-side component to create? WebPart
Add new Web part to solution helloworld-webpart.
? What is your Web part name? HelloWorld
? What is your Web part description? HelloWorld description
? Which framework would you like to use? No JavaScript framework

   create package.json
   create config\package-solution.json
   create config\config.json
   create config\serve.json
   create tsconfig.json
   create .vscode\extensions.json
   create .vscode\launch.json
   create .vscode\settings.json
   create config\copy-assets.json
   create config\deploy-azure-storage.json
   create config\write-manifests.json
   create src\index.ts
   create gulpfile.js
   create README.md
   create tslint.json
   create .editorconfig
   create .gitignore
   create src\webparts\helloWorld\HelloWorldWebPart.module.scss
   create src\webparts\helloWorld\HelloWorldWebPart.ts
   create src\webparts\helloWorld\loc\en-us.js
   create src\webparts\helloWorld\loc\mystrings.d.ts
   create src\webparts\helloWorld\HelloWorldWebPart.manifest.json
   create teams\75d8c609-d226-4c87-aa15-d028fd4c3692_outline.png
   create teams\75d8c609-d226-4c87-aa15-d028fd4c3692_color.png

npm WARN deprecated gulp-util@3.0.8: gulp-util is deprecated - replace it, following the guidelines at https://medium.com/gulpjs/gulp-util-ca3b1f9f9ac5
npm WARN deprecated minimatch@2.0.10: Please update to minimatch 3.0.2 or higher to avoid a RegExp DoS issue
npm WARN deprecated natives@1.1.6: This module relies on Node.js's internals and will break at some point. Do not use it, and update to graceful-fs@4.x.
npm WARN deprecated request@2.88.2: request has been deprecated, see https://github.com/request/request/issues/3142
npm WARN deprecated chokidar@2.1.8: Chokidar 2 will break on node v14+. Upgrade to chokidar 3 with 15x less dependencies.
npm WARN deprecated left-pad@1.3.0: use String.prototype.padStart()
npm WARN deprecated request-promise-native@1.0.9: request-promise-native has been deprecated because it extends the now deprecated request package, see https://github.com/request/request/issues/3142
npm WARN deprecated core-js@1.2.7: core-js@<3 is no longer maintained and not recommended for usage due to the number of issues. Please, upgrade your dependencies to the actual version of core-js@3.
npm WARN deprecated har-validator@5.1.5: this library is no longer supported
npm WARN deprecated fsevents@1.2.13: fsevents 1 will break on node v14+ and could be using insecure binaries. Upgrade to fsevents 2.
npm WARN deprecated es6-collections@0.5.6: not actively maintained anymore
npm WARN deprecated minimatch@0.2.14: Please update to minimatch 3.0.2 or higher to avoid a RegExp DoS issue
npm WARN deprecated mkdirp@0.5.1: Legacy versions of mkdirp are no longer supported. Please update to mkdirp 1.x. (Note that the API surface has changed to use Promises in 1.x.)
npm WARN deprecated resolve-url@0.2.1: https://github.com/lydell/resolve-url#deprecated
npm WARN deprecated urix@0.1.0: Please see https://github.com/lydell/urix#deprecated
npm WARN deprecated kleur@2.0.2: Please upgrade to kleur@3 or migrate to 'ansi-colors' if you prefer the old syntax. Visit <https://github.com/lukeed/kleur/releases/tag/v3.0.0\> for migration path(s).
npm WARN deprecated graceful-fs@1.2.3: please upgrade to graceful-fs 4 for compatibility with current and future versions of Node.js
npm WARN deprecated core-js@2.6.12: core-js@<3 is no longer maintained and not recommended for usage due to the number of issues. Please, upgrade your dependencies to the actual version of core-js@3.
npm WARN deprecated mkdirp-promise@5.0.1: This package is broken and no longer maintained. 'mkdirp' itself supports promises now, please switch to that.

> deasync@0.1.21 install D:\code\helloworld-webpart\node_modules\deasync
> node ./build.js

`win32-x64-node-14` exists; testing
Binary is fine; exiting

> node-sass@4.12.0 install D:\code\helloworld-webpart\node_modules\node-sass
> node scripts/install.js

Downloading binary from https://github.com/sass/node-sass/releases/download/v4.12.0/win32-x64-83_binding.node
Cannot download "https://github.com/sass/node-sass/releases/download/v4.12.0/win32-x64-83_binding.node":

HTTP error 404 Not Found

Hint: If github.com is not accessible in your location
      try setting a proxy via HTTP_PROXY, e.g.

      export HTTP_PROXY=http://example.com:1234

or configure npm proxy via

      npm config set proxy http://example.com:8080

> core-js@2.6.12 postinstall D:\code\helloworld-webpart\node_modules\core-js
> node -e "try{require('./postinstall')}catch(e){}"

Thank you for using core-js ( https://github.com/zloirock/core-js ) for polyfilling JavaScript standard library!

The project needs your help! Please consider supporting of core-js on Open Collective or Patreon:
> https://opencollective.com/core-js
> https://www.patreon.com/zloirock

Also, the author of core-js ( https://github.com/zloirock ) is looking for a good job -)


> uglifyjs-webpack-plugin@0.4.6 postinstall D:\code\helloworld-webpart\node_modules\uglifyjs-webpack-plugin
> node lib/post_install.js


> node-sass@4.12.0 postinstall D:\code\helloworld-webpart\node_modules\node-sass
> node scripts/build.js

Building: C:\Program Files\nodejs\node.exe D:\code\helloworld-webpart\node_modules\node-gyp\bin\node-gyp.js rebuild --verbose --libsass_ext= --libsass_cflags= --libsass_ldflags= --libsass_library=
gyp info it worked if it ends with ok
gyp verb cli [
gyp verb cli   'C:\\Program Files\\nodejs\\node.exe',
gyp verb cli   'D:\\code\\helloworld-webpart\\node_modules\\node-gyp\\bin\\node-gyp.js',
gyp verb cli   'rebuild',
gyp verb cli   '--verbose',
gyp verb cli   '--libsass_ext=',
gyp verb cli   '--libsass_cflags=',
gyp verb cli   '--libsass_ldflags=',
gyp verb cli   '--libsass_library='
gyp verb cli ]
gyp info using node-gyp@3.8.0
gyp info using node@14.16.1 | win32 | x64
gyp verb command rebuild []
gyp verb command clean []
gyp verb clean removing "build" directory
gyp verb command configure []
gyp verb check python checking for Python executable "python2" in the PATH
gyp verb `which` failed Error: not found: python2
gyp verb `which` failed     at getNotFoundError (D:\code\helloworld-webpart\node_modules\which\which.js:13:12)
gyp verb `which` failed     at F (D:\code\helloworld-webpart\node_modules\which\which.js:68:19)
gyp verb `which` failed     at E (D:\code\helloworld-webpart\node_modules\which\which.js:80:29)
gyp verb `which` failed     at D:\code\helloworld-webpart\node_modules\which\which.js:89:16
gyp verb `which` failed     at D:\code\helloworld-webpart\node_modules\isexe\index.js:42:5
gyp verb `which` failed     at D:\code\helloworld-webpart\node_modules\isexe\windows.js:36:5
gyp verb `which` failed     at FSReqCallback.oncomplete (fs.js:183:21)
gyp verb `which` failed  python2 Error: not found: python2
gyp verb `which` failed     at getNotFoundError (D:\code\helloworld-webpart\node_modules\which\which.js:13:12)
gyp verb `which` failed     at F (D:\code\helloworld-webpart\node_modules\which\which.js:68:19)
gyp verb `which` failed     at E (D:\code\helloworld-webpart\node_modules\which\which.js:80:29)
gyp verb `which` failed     at D:\code\helloworld-webpart\node_modules\which\which.js:89:16
gyp verb `which` failed     at D:\code\helloworld-webpart\node_modules\isexe\index.js:42:5
gyp verb `which` failed     at D:\code\helloworld-webpart\node_modules\isexe\windows.js:36:5
gyp verb `which` failed     at FSReqCallback.oncomplete (fs.js:183:21) {
gyp verb `which` failed   code: 'ENOENT'
gyp verb `which` failed }
gyp verb check python checking for Python executable "python" in the PATH
gyp verb `which` failed Error: not found: python
gyp verb `which` failed     at getNotFoundError (D:\code\helloworld-webpart\node_modules\which\which.js:13:12)
gyp verb `which` failed     at F (D:\code\helloworld-webpart\node_modules\which\which.js:68:19)
gyp verb `which` failed     at E (D:\code\helloworld-webpart\node_modules\which\which.js:80:29)
gyp verb `which` failed     at D:\code\helloworld-webpart\node_modules\which\which.js:89:16
gyp verb `which` failed     at D:\code\helloworld-webpart\node_modules\isexe\index.js:42:5
gyp verb `which` failed     at D:\code\helloworld-webpart\node_modules\isexe\windows.js:36:5
gyp verb `which` failed     at FSReqCallback.oncomplete (fs.js:183:21)
gyp verb `which` failed  python Error: not found: python
gyp verb `which` failed     at getNotFoundError (D:\code\helloworld-webpart\node_modules\which\which.js:13:12)
gyp verb `which` failed     at F (D:\code\helloworld-webpart\node_modules\which\which.js:68:19)
gyp verb `which` failed     at E (D:\code\helloworld-webpart\node_modules\which\which.js:80:29)
gyp verb `which` failed     at D:\code\helloworld-webpart\node_modules\which\which.js:89:16
gyp verb `which` failed     at D:\code\helloworld-webpart\node_modules\isexe\index.js:42:5
gyp verb `which` failed     at D:\code\helloworld-webpart\node_modules\isexe\windows.js:36:5
gyp verb `which` failed     at FSReqCallback.oncomplete (fs.js:183:21) {
gyp verb `which` failed   code: 'ENOENT'
gyp verb `which` failed }
gyp verb could not find "python". checking python launcher
gyp verb could not find "python". guessing location
gyp verb ensuring that file exists: C:\Python27\python.exe
gyp ERR! configure error
gyp ERR! stack Error: Can't find Python executable "python", you can set the PYTHON env variable.
gyp ERR! stack     at PythonFinder.failNoPython (D:\code\helloworld-webpart\node_modules\node-gyp\lib\configure.js:484:19)
gyp ERR! stack     at PythonFinder.<anonymous> (D:\code\helloworld-webpart\node_modules\node-gyp\lib\configure.js:509:16)
gyp ERR! stack     at callback (D:\code\helloworld-webpart\node_modules\graceful-fs\polyfills.js:299:20)
gyp ERR! stack     at FSReqCallback.oncomplete (fs.js:183:21)
gyp ERR! System Windows_NT 10.0.19041
gyp ERR! command "C:\\Program Files\\nodejs\\node.exe" "D:\\code\\helloworld-webpart\\node_modules\\node-gyp\\bin\\node-gyp.js" "rebuild" "--verbose" "--libsass_ext=" "--libsass_cflags=" "--libsass_ldflags=" "--libsass_library="
gyp ERR! cwd D:\code\helloworld-webpart\node_modules\node-sass
gyp ERR! node -v v14.16.1
gyp ERR! node-gyp -v v3.8.0
gyp ERR! not ok
Build failed with error code: 1
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@^1.2.7 (node_modules\chokidar\node_modules\fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@1.2.13: wanted {"os":"darwin","arch":"any"} (current: {"os":"win32","arch":"x64"})
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@~2.3.1 (node_modules\watchpack\node_modules\chokidar\node_modules\fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@2.3.2: wanted {"os":"darwin","arch":"any"} (current: {"os":"win32","arch":"x64"})
npm WARN ajv-keywords@3.5.2 requires a peer of ajv@^6.9.1 but none is installed. You must install peer dependencies yourself.
npm WARN uglifyjs-webpack-plugin@0.4.6 requires a peer of webpack@^1.9 || ^2 || ^2.1.0-beta || ^2.2.0-rc || ^3.0.0 but none is installed. You must install peer dependencies yourself.

npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! node-sass@4.12.0 postinstall: `node scripts/build.js`
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the node-sass@4.12.0 postinstall script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.

npm ERR! A complete log of this run can be found in:
npm ERR!     C:\Users\krnotes\AppData\Roaming\npm-cache\_logs\2021-04-10T14_56_33_082Z-debug.log

      _=+#####!
   ###########|       .-------------------------------------------.
   ###/    (##|(@)    |              Congratulations!             |
   ###  ######|   \   |  Solution helloworld-webpart is created.  |
   ###/   /###|   (@) |      Run gulp serve to play with it!      |
   #######  ##|   /   '-------------------------------------------'
   ###     /##|(@)
   ###########|
      **=+####!


D:\code\helloworld-webpart>
D:\code\helloworld-webpart>gulp trust-dev-cert
Error: Cannot find module '@microsoft/sp-build-web'
Require stack:
- D:\code\helloworld-webpart\gulpfile.js
- C:\Users\krnotes\AppData\Roaming\npm\node_modules\gulp\node_modules\gulp-cli\lib\shared\require-or-import.js
- C:\Users\krnotes\AppData\Roaming\npm\node_modules\gulp\node_modules\gulp-cli\lib\versioned\^3.7.0\index.js
- C:\Users\krnotes\AppData\Roaming\npm\node_modules\gulp\node_modules\gulp-cli\index.js
- C:\Users\krnotes\AppData\Roaming\npm\node_modules\gulp\bin\gulp.js
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:880:15)
    at Function.Module._load (internal/modules/cjs/loader.js:725:27)
    at Module.require (internal/modules/cjs/loader.js:952:19)
    at require (internal/modules/cjs/helpers.js:88:18)
    at Object.<anonymous> (D:\code\helloworld-webpart\gulpfile.js:3:15)
    at Module._compile (internal/modules/cjs/loader.js:1063:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
    at Module.load (internal/modules/cjs/loader.js:928:32)
    at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    at Module.require (internal/modules/cjs/loader.js:952:19) {
  code: 'MODULE_NOT_FOUND',
  requireStack: [
    'D:\\code\\helloworld-webpart\\gulpfile.js',
    'C:\\Users\\krnotes\\AppData\\Roaming\\npm\\node_modules\\gulp\\node_modules\\gulp-cli\\lib\\shared\\require-or-import.js',
    'C:\\Users\\krnotes\\AppData\\Roaming\\npm\\node_modules\\gulp\\node_modules\\gulp-cli\\lib\\versioned\\^3.7.0\\index.js',
    'C:\\Users\\krnotes\\AppData\\Roaming\\npm\\node_modules\\gulp\\node_modules\\gulp-cli\\index.js',
    'C:\\Users\\krnotes\\AppData\\Roaming\\npm\\node_modules\\gulp\\bin\\gulp.js'
  ]
}

D:\code\helloworld-webpart>

```



# api documentation for  [ember-websockets (v7.0.2)](https://github.com/thoov/ember-websockets#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-ember-websockets.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-ember-websockets) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-ember-websockets.svg)](https://travis-ci.org/npmdoc/node-npmdoc-ember-websockets)
#### EmberJS WebSockets addon for Ember-CLI apps.

[![NPM](https://nodei.co/npm/ember-websockets.png?downloads=true)](https://www.npmjs.com/package/ember-websockets)

[![apidoc](https://npmdoc.github.io/node-npmdoc-ember-websockets/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-ember-websockets_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-ember-websockets/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-ember-websockets/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-ember-websockets/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Travis Hoover",
        "email": "thoov7@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/thoov/ember-websockets/issues"
    },
    "dependencies": {
        "broccoli-funnel": "^1.0.1",
        "broccoli-merge-trees": "^2.0.0",
        "ember-cli-babel": "^5.1.7",
        "exists-sync": "0.0.4",
        "mock-socket": "^6.0.1",
        "socket.io-client": "^1.7.3",
        "urijs": "^1.18.9"
    },
    "description": "EmberJS WebSockets addon for Ember-CLI apps.",
    "devDependencies": {
        "broccoli-asset-rev": "^2.4.5",
        "ember-ajax": "^2.4.1",
        "ember-cli": "2.12.0",
        "ember-cli-code-coverage": "^0.3.11",
        "ember-cli-dependency-checker": "^1.3.0",
        "ember-cli-eslint": "^3.0.0",
        "ember-cli-htmlbars": "^1.1.1",
        "ember-cli-htmlbars-inline-precompile": "^0.3.6",
        "ember-cli-inject-live-reload": "^1.4.1",
        "ember-cli-qunit": "^3.1.0",
        "ember-cli-shims": "^1.0.2",
        "ember-cli-sri": "^2.1.0",
        "ember-cli-uglify": "^1.2.0",
        "ember-disable-prototype-extensions": "^1.1.0",
        "ember-export-application-global": "^1.0.5",
        "ember-load-initializers": "^0.6.0",
        "ember-resolver": "^2.0.3",
        "ember-source": "~2.12.0",
        "loader.js": "^4.2.3"
    },
    "directories": {
        "addon": "addon",
        "app": "app",
        "doc": "doc",
        "test": "tests"
    },
    "dist": {
        "shasum": "be5500e741b5665619e1b047f5386bc4769f5fee",
        "tarball": "https://registry.npmjs.org/ember-websockets/-/ember-websockets-7.0.2.tgz"
    },
    "ember-addon": {
        "configPath": "tests/dummy/config"
    },
    "engines": {
        "node": ">= 4"
    },
    "gitHead": "c03fc231c7359a8ee23eda5d079440a3cab58c5f",
    "homepage": "https://github.com/thoov/ember-websockets#readme",
    "keywords": [
        "ember-addon",
        "websockets",
        "sockets",
        "web sockets",
        "ember websockets",
        "emberjs websockets"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "thoov",
            "email": "thoov7@gmail.com"
        }
    ],
    "name": "ember-websockets",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/thoov/ember-websockets.git"
    },
    "scripts": {
        "build": "ember build",
        "start": "ember server",
        "test": "ember try:each"
    },
    "version": "7.0.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module ember-websockets](#apidoc.module.ember-websockets)
1.  [function <span class="apidocSignatureSpan">ember-websockets.</span>_isFastbootBuild ()](#apidoc.element.ember-websockets._isFastbootBuild)
1.  [function <span class="apidocSignatureSpan">ember-websockets.</span>_readConfig (environment)](#apidoc.element.ember-websockets._readConfig)
1.  [function <span class="apidocSignatureSpan">ember-websockets.</span>_readConfigProp (prop)](#apidoc.element.ember-websockets._readConfigProp)
1.  [function <span class="apidocSignatureSpan">ember-websockets.</span>_shimImport ()](#apidoc.element.ember-websockets._shimImport)
1.  [function <span class="apidocSignatureSpan">ember-websockets.</span>included ()](#apidoc.element.ember-websockets.included)
1.  [function <span class="apidocSignatureSpan">ember-websockets.</span>treeForVendor ()](#apidoc.element.ember-websockets.treeForVendor)
1.  string <span class="apidocSignatureSpan">ember-websockets.</span>name



# <a name="apidoc.module.ember-websockets"></a>[module ember-websockets](#apidoc.module.ember-websockets)

#### <a name="apidoc.element.ember-websockets._isFastbootBuild"></a>[function <span class="apidocSignatureSpan">ember-websockets.</span>_isFastbootBuild ()](#apidoc.element.ember-websockets._isFastbootBuild)
- description and source-code
```javascript
_isFastbootBuild() {
  return !!process.env.EMBER_CLI_FASTBOOT;
}
```
- example usage
```shell
...
module.exports = {
name: 'ember-websockets',

included() {
  this._super.included.apply(this, arguments);
  this._shimImport();

  if (!this._isFastbootBuild()) {
    this.import('vendor/${this.name}/urijs/URI.min.js');

    if (this._readConfigProp('socketIO') === true) {
      this.import('vendor/${this.name}/socket.io-client/socket.io.min.js');
    }
  }
},
...
```

#### <a name="apidoc.element.ember-websockets._readConfig"></a>[function <span class="apidocSignatureSpan">ember-websockets.</span>_readConfig (environment)](#apidoc.element.ember-websockets._readConfig)
- description and source-code
```javascript
_readConfig(environment) {
  const project = this.app.project;

  // NOTE: For ember-cli >= 2.6.0-beta.3, project.configPath() returns absolute path
  // while older ember-cli versions return path relative to project root
  const configPath = path.dirname(project.configPath());
  let config = path.join(configPath, 'environment.js');

  if (!path.isAbsolute(config)) {
    config = path.join(project.root, config);
  }

  if (exists(config)) {
    return require(config)(environment);
  }

  return {
    'ember-websockets': {}
  };
}
```
- example usage
```shell
...
  return {
    'ember-websockets': {}
  };
},

_readConfigProp(prop) {
  this._shimImport();
  const config = this._readConfig(this._findHost().env);

  if (config['ember-websockets'] && config['ember-websockets'][prop]) {
    return config['ember-websockets'][prop];
  }
},

_isFastbootBuild() {
...
```

#### <a name="apidoc.element.ember-websockets._readConfigProp"></a>[function <span class="apidocSignatureSpan">ember-websockets.</span>_readConfigProp (prop)](#apidoc.element.ember-websockets._readConfigProp)
- description and source-code
```javascript
_readConfigProp(prop) {
  this._shimImport();
  const config = this._readConfig(this._findHost().env);

  if (config['ember-websockets'] && config['ember-websockets'][prop]) {
    return config['ember-websockets'][prop];
  }
}
```
- example usage
```shell
...
included() {
  this._super.included.apply(this, arguments);
  this._shimImport();

  if (!this._isFastbootBuild()) {
    this.import('vendor/${this.name}/urijs/URI.min.js');

    if (this._readConfigProp('socketIO') === true) {
      this.import('vendor/${this.name}/socket.io-client/socket.io.min.js');
    }
  }
},

treeForVendor() {
  const urijsPath = require.resolve('urijs');
...
```

#### <a name="apidoc.element.ember-websockets._shimImport"></a>[function <span class="apidocSignatureSpan">ember-websockets.</span>_shimImport ()](#apidoc.element.ember-websockets._shimImport)
- description and source-code
```javascript
_shimImport() {
  if (!this.import) {
    this._findHost = function findHostShim() {
      let current = this;
      let app;
      do {
        app = current.app || app;
      } while (current.parent.parent && (current = current.parent));
      return app;
    };
    this.import = function importShim(asset, options) {
      const app = this._findHost();
      app.import(asset, options);
    };
  }
}
```
- example usage
```shell
...
const Merge = require('broccoli-merge-trees');

module.exports = {
  name: 'ember-websockets',

  included() {
    this._super.included.apply(this, arguments);
    this._shimImport();

    if (!this._isFastbootBuild()) {
this.import('vendor/${this.name}/urijs/URI.min.js');

if (this._readConfigProp('socketIO') === true) {
  this.import('vendor/${this.name}/socket.io-client/socket.io.min.js');
}
...
```

#### <a name="apidoc.element.ember-websockets.included"></a>[function <span class="apidocSignatureSpan">ember-websockets.</span>included ()](#apidoc.element.ember-websockets.included)
- description and source-code
```javascript
included() {
  this._super.included.apply(this, arguments);
  this._shimImport();

  if (!this._isFastbootBuild()) {
    this.import('vendor/${this.name}/urijs/URI.min.js');

    if (this._readConfigProp('socketIO') === true) {
      this.import('vendor/${this.name}/socket.io-client/socket.io.min.js');
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ember-websockets.treeForVendor"></a>[function <span class="apidocSignatureSpan">ember-websockets.</span>treeForVendor ()](#apidoc.element.ember-websockets.treeForVendor)
- description and source-code
```javascript
treeForVendor() {
  const urijsPath = require.resolve('urijs');
  const mockSocketPath = require.resolve('mock-socket');
  const socketIOClientPath = require.resolve('socket.io-client');

  return new Merge([
    new Funnel(__dirname + '/vendor', { destDir: this.name }),
    new Funnel(path.dirname(urijsPath), { destDir: this.name + '/urijs' }),
    new Funnel(path.dirname(mockSocketPath), { destDir: this.name + '/mock-socket' }),
    new Funnel(path.join(path.dirname(socketIOClientPath), '../dist'), { destDir: this.name + '/socket.io-client' })
  ]);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

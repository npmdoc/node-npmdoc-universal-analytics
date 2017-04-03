# api documentation for  [universal-analytics (v0.4.13)](https://github.com/peaksandpies/universal-analytics#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-universal-analytics.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-universal-analytics) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-universal-analytics.svg)](https://travis-ci.org/npmdoc/node-npmdoc-universal-analytics)
#### A node module for Google's Universal Analytics tracking

[![NPM](https://nodei.co/npm/universal-analytics.png?downloads=true)](https://www.npmjs.com/package/universal-analytics)

[![apidoc](https://npmdoc.github.io/node-npmdoc-universal-analytics/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-universal-analytics_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-universal-analytics/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-universal-analytics/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-universal-analytics/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jörg Tillmann",
        "email": "joerg@peaksandpies.com"
    },
    "bugs": {
        "url": "https://github.com/peaksandpies/universal-analytics/issues"
    },
    "dependencies": {
        "async": "1.2.x",
        "request": "2.x",
        "underscore": "1.x",
        "uuid": "^3.0.0"
    },
    "description": "A node module for Google's Universal Analytics tracking",
    "devDependencies": {
        "mocha": "*",
        "should": "*",
        "sinon": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "dc6829ff7297ae1b4f8d1427d5a945521f1bba26",
        "tarball": "https://registry.npmjs.org/universal-analytics/-/universal-analytics-0.4.13.tgz"
    },
    "gitHead": "875b6943c0989e5ab1a14cde62f44cc323f0d54c",
    "homepage": "https://github.com/peaksandpies/universal-analytics#readme",
    "keywords": [
        "google",
        "analytics",
        "universal",
        "tracking"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "jtillmann",
            "email": "mail@joergtillmann.com"
        }
    ],
    "name": "universal-analytics",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/peaksandpies/universal-analytics.git"
    },
    "scripts": {
        "test": "make test"
    },
    "version": "0.4.13"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module universal-analytics](#apidoc.module.universal-analytics)
1.  [function <span class="apidocSignatureSpan">universal-analytics.</span>Visitor (tid, cid, options, context, persistentParams)](#apidoc.element.universal-analytics.Visitor)
1.  [function <span class="apidocSignatureSpan">universal-analytics.</span>createFromSession (session)](#apidoc.element.universal-analytics.createFromSession)
1.  [function <span class="apidocSignatureSpan">universal-analytics.</span>middleware (tid, options)](#apidoc.element.universal-analytics.middleware)
1.  object <span class="apidocSignatureSpan">universal-analytics.</span>Visitor.prototype
1.  object <span class="apidocSignatureSpan">universal-analytics.</span>utils

#### [module universal-analytics.Visitor](#apidoc.module.universal-analytics.Visitor)
1.  [function <span class="apidocSignatureSpan">universal-analytics.</span>Visitor (tid, cid, options, context, persistentParams)](#apidoc.element.universal-analytics.Visitor.Visitor)

#### [module universal-analytics.Visitor.prototype](#apidoc.module.universal-analytics.Visitor.prototype)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_checkParameters (params)](#apidoc.element.universal-analytics.Visitor.prototype._checkParameters)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_determineCid ()](#apidoc.element.universal-analytics.Visitor.prototype._determineCid)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_enqueue (type, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype._enqueue)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_handleError (message, fn)](#apidoc.element.universal-analytics.Visitor.prototype._handleError)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_log (message)](#apidoc.element.universal-analytics.Visitor.prototype._log)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_tidyParameters (params)](#apidoc.element.universal-analytics.Visitor.prototype._tidyParameters)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_translateParams (params)](#apidoc.element.universal-analytics.Visitor.prototype._translateParams)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_withContext (context)](#apidoc.element.universal-analytics.Visitor.prototype._withContext)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>debug (debug)](#apidoc.element.universal-analytics.Visitor.prototype.debug)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>e (category, action, label, value, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.e)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>event (category, action, label, value, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.event)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>exception (description, fatal, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.exception)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>i (price, quantity, sku, name, variation, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.i)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>item (price, quantity, sku, name, variation, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.item)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>pageview (path, hostname, title, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.pageview)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>pv (path, hostname, title, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.pv)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>reset ()](#apidoc.element.universal-analytics.Visitor.prototype.reset)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>screenview (screenName, appName, appVersion, appId, appInstallerId, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.screenview)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>send (fn)](#apidoc.element.universal-analytics.Visitor.prototype.send)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>set (key, value)](#apidoc.element.universal-analytics.Visitor.prototype.set)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>t (transaction, revenue, shipping, tax, affiliation, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.t)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>timing (category, variable, time, label, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.timing)
1.  [function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>transaction (transaction, revenue, shipping, tax, affiliation, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.transaction)

#### [module universal-analytics.utils](#apidoc.module.universal-analytics.utils)
1.  [function <span class="apidocSignatureSpan">universal-analytics.utils.</span>ensureValidCid (uuid)](#apidoc.element.universal-analytics.utils.ensureValidCid)
1.  [function <span class="apidocSignatureSpan">universal-analytics.utils.</span>isCookieCid (cid)](#apidoc.element.universal-analytics.utils.isCookieCid)
1.  [function <span class="apidocSignatureSpan">universal-analytics.utils.</span>isUuid (uuid)](#apidoc.element.universal-analytics.utils.isUuid)



# <a name="apidoc.module.universal-analytics"></a>[module universal-analytics](#apidoc.module.universal-analytics)

#### <a name="apidoc.element.universal-analytics.Visitor"></a>[function <span class="apidocSignatureSpan">universal-analytics.</span>Visitor (tid, cid, options, context, persistentParams)](#apidoc.element.universal-analytics.Visitor)
- description and source-code
```javascript
Visitor = function (tid, cid, options, context, persistentParams) {

  if (typeof tid === 'object') {
    options = tid;
    tid = cid = null;
  } else if (typeof cid === 'object') {
    options = cid;
    cid = null;
  }

  this._queue = [];

  this.options = options || {};

  if(this.options.hostname) {
    config.hostname = this.options.hostname;
  }
  if(this.options.path) {
    config.path = this.options.path;
  }

  if (this.options.https) {
    var parsedHostname = url.parse(config.hostname);
    config.hostname = 'https://' + parsedHostname.host;
  }

  if(this.options.enableBatching !== undefined) {
    config.batching = options.enableBatching;
  }

  if(this.options.batchSize) {
    config.batchSize = this.options.batchSize;
  }

  this._context = context || {};
  this._persistentParams = persistentParams || {};

  this.tid = tid || this.options.tid;
  this.cid = this._determineCid(cid, this.options.cid, (this.options.strictCidFormat !== false));
  if(this.options.uid) {
    this.uid = this.options.uid;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.createFromSession"></a>[function <span class="apidocSignatureSpan">universal-analytics.</span>createFromSession (session)](#apidoc.element.universal-analytics.createFromSession)
- description and source-code
```javascript
createFromSession = function (session) {
  if (session && session.cid) {
    return init(this.tid, session.cid, this.options);
  }
}
```
- example usage
```shell
...
'''

The middleware will attach the 'universal analytics' visitor instance to every request ('req.visitor').

Additionally, the module also exposes a 'createFromSession' method to create a visitor instance simply based on a session, which
 is helpful when working with Socket.io, etc. where the middleware is not used.

'''javascript
var visitor = ua.createFromSession(socket.handshake.session);
'''

# Debug mode

'universal-analytics' can be instructed to output information during tracking by enabling the debug mode:

'''javascript
...
```

#### <a name="apidoc.element.universal-analytics.middleware"></a>[function <span class="apidocSignatureSpan">universal-analytics.</span>middleware (tid, options)](#apidoc.element.universal-analytics.middleware)
- description and source-code
```javascript
middleware = function (tid, options) {

  this.tid = tid;
  this.options = options;

  var cookieName = (this.options || {}).cookieName || "_ga";

  return function (req, res, next) {

    req.visitor = module.exports.createFromSession(req.session);

    if (req.visitor) return next();

    var cid;
    if (req.cookies && req.cookies[cookieName]) {
      var gaSplit = req.cookies[cookieName].split('.');
      cid = gaSplit[2] + "." + gaSplit[3];
    }

    req.visitor = init(tid, cid, options);

    if (req.session) {
      req.session.cid = req.visitor.cid;
    }

    next();
  }
}
```
- example usage
```shell
...

'''javascript
var ua = require("universal-analytics");
var express = require("express");

var app = express()

express.use(ua.middleware("UA-XXXX-Y", {cookieName: '_ga'}));
'''

The middleware will attach the 'universal analytics' visitor instance to every request ('req.visitor').

Additionally, the module also exposes a 'createFromSession' method to create a visitor instance simply based on a session, which
 is helpful when working with Socket.io, etc. where the middleware is not used.

'''javascript
...
```



# <a name="apidoc.module.universal-analytics.Visitor"></a>[module universal-analytics.Visitor](#apidoc.module.universal-analytics.Visitor)

#### <a name="apidoc.element.universal-analytics.Visitor.Visitor"></a>[function <span class="apidocSignatureSpan">universal-analytics.</span>Visitor (tid, cid, options, context, persistentParams)](#apidoc.element.universal-analytics.Visitor.Visitor)
- description and source-code
```javascript
Visitor = function (tid, cid, options, context, persistentParams) {

  if (typeof tid === 'object') {
    options = tid;
    tid = cid = null;
  } else if (typeof cid === 'object') {
    options = cid;
    cid = null;
  }

  this._queue = [];

  this.options = options || {};

  if(this.options.hostname) {
    config.hostname = this.options.hostname;
  }
  if(this.options.path) {
    config.path = this.options.path;
  }

  if (this.options.https) {
    var parsedHostname = url.parse(config.hostname);
    config.hostname = 'https://' + parsedHostname.host;
  }

  if(this.options.enableBatching !== undefined) {
    config.batching = options.enableBatching;
  }

  if(this.options.batchSize) {
    config.batchSize = this.options.batchSize;
  }

  this._context = context || {};
  this._persistentParams = persistentParams || {};

  this.tid = tid || this.options.tid;
  this.cid = this._determineCid(cid, this.options.cid, (this.options.strictCidFormat !== false));
  if(this.options.uid) {
    this.uid = this.options.uid;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.universal-analytics.Visitor.prototype"></a>[module universal-analytics.Visitor.prototype](#apidoc.module.universal-analytics.Visitor.prototype)

#### <a name="apidoc.element.universal-analytics.Visitor.prototype._checkParameters"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_checkParameters (params)](#apidoc.element.universal-analytics.Visitor.prototype._checkParameters)
- description and source-code
```javascript
_checkParameters = function (params) {
  for (var param in params) {
    if (config.acceptedParameters.indexOf(param) !== -1 || config.acceptedParametersRegex.filter(function (r) {
        return r.test(param);
      }).length) {
      continue;
    }
    this._log("Warning! Unsupported tracking parameter " + param + " (" + params[param] + ")");
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype._determineCid"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_determineCid ()](#apidoc.element.universal-analytics.Visitor.prototype._determineCid)
- description and source-code
```javascript
_determineCid = function () {
  var args = Array.prototype.splice.call(arguments, 0);
  var id;
  var lastItem = args.length-1;
  var strict = args[lastItem];
  if (strict) {
    for (var i = 0; i < lastItem; i++) {
      id = utils.ensureValidCid(args[i]);
      if (id !== false) return id;
      if (id != null) this._log("Warning! Invalid UUID format '" + args[i] + "'");
    }
  } else {
    for (var i = 0; i < lastItem; i++) {
      if (args[i]) return args[i];
    }
  }
  return uuid.v4();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype._enqueue"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_enqueue (type, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype._enqueue)
- description and source-code
```javascript
_enqueue = function (type, params, fn) {

  if (typeof params === 'function') {
    fn = params;
    params = {};
  }

  params = this._translateParams(params) || {};

  _.extend(params, {
    v: config.protocolVersion,
    tid: this.tid,
    cid: this.cid,
    t: type
  });
  if(this.uid) {
    params.uid = this.uid;
  }

  this._queue.push(params);

  if (this.options.debug) {
    this._checkParameters(params);
  }

  this._log("Enqueued " + type + " (" + JSON.stringify(params) + ")");

  if (fn) {
    this.send(fn);
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype._handleError"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_handleError (message, fn)](#apidoc.element.universal-analytics.Visitor.prototype._handleError)
- description and source-code
```javascript
_handleError = function (message, fn) {
    this._log("Error: " + message)
    fn && fn.call(this, new Error(message))
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype._log"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_log (message)](#apidoc.element.universal-analytics.Visitor.prototype._log)
- description and source-code
```javascript
_log = function (message) {
  this.options.debug && console.log("[universal-analytics] " + message);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype._tidyParameters"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_tidyParameters (params)](#apidoc.element.universal-analytics.Visitor.prototype._tidyParameters)
- description and source-code
```javascript
_tidyParameters = function (params) {
  for (var param in params) {
    if (params[param] === null || params[param] === undefined) {
      delete params[param];
    }
  }
  return params;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype._translateParams"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_translateParams (params)](#apidoc.element.universal-analytics.Visitor.prototype._translateParams)
- description and source-code
```javascript
_translateParams = function (params) {
    var translated = {};
    for (var key in params) {
        if (config.parametersMap.hasOwnProperty(key)) {
            translated[config.parametersMap[key]] = params[key];
        } else {
            translated[key] = params[key];
        }
    }
    return translated;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype._withContext"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>_withContext (context)](#apidoc.element.universal-analytics.Visitor.prototype._withContext)
- description and source-code
```javascript
_withContext = function (context) {
  var visitor = new Visitor(this.tid, this.cid, this.options, context, this._persistentParams);
  visitor._queue = this._queue;
  return visitor;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.debug"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>debug (debug)](#apidoc.element.universal-analytics.Visitor.prototype.debug)
- description and source-code
```javascript
debug = function (debug) {
  this.options.debug = arguments.length === 0 ? true : debug;
  this._log("Logging enabled")
  return this;
}
```
- example usage
```shell
...
'''

# Debug mode

'universal-analytics' can be instructed to output information during tracking by enabling the debug mode:

'''javascript
var visitor = ua("UA-XXXX-XX").debug()
// … and so forth.
'''


# Request Options

In order to add additional options to the request a 'requestOptions' hash can be provided as part of the constructor options. 'unviversal
-analytics' uses the ['request'](https://www.npmjs.com/package/request) library. Therefor [any option available for that library
](https://www.npmjs.com/package/request#requestoptions-callback) can be provided via the 'requestOptions'.
...
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.e"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>e (category, action, label, value, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.e)
- description and source-code
```javascript
e = function (category, action, label, value, params, fn) {

  if (typeof category === 'object' && category != null) {
    params = category;
    if (typeof action === 'function') {
      fn = action
    }
    category = action = label = value = null;
  } else if (typeof label === 'function') {
    fn = label;
    label = value = null;
  } else if (typeof value === 'function') {
    fn = value;
    value = null;
  } else if (typeof params === 'function') {
    fn = params;
    params = null;
  }

  params = this._translateParams(params);

  params = _.extend({}, this._persistentParams || {}, params);

  params.ec = category || params.ec || this._context.ec;
  params.ea = action || params.ea || this._context.ea;
  params.el = label || params.el || this._context.el;
  params.ev = value || params.ev || this._context.ev;
  params.p = params.p || params.dp || this._context.p || this._context.dp;

  delete params.dp;
  this._tidyParameters(params);

  if (!params.ec || !params.ea) {
    return this._handleError("Please provide at least an event category (ec) and an event action (ea)", fn);
  }

  return this._withContext(params)._enqueue("event", params, fn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.event"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>event (category, action, label, value, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.event)
- description and source-code
```javascript
event = function (category, action, label, value, params, fn) {

  if (typeof category === 'object' && category != null) {
    params = category;
    if (typeof action === 'function') {
      fn = action
    }
    category = action = label = value = null;
  } else if (typeof label === 'function') {
    fn = label;
    label = value = null;
  } else if (typeof value === 'function') {
    fn = value;
    value = null;
  } else if (typeof params === 'function') {
    fn = params;
    params = null;
  }

  params = this._translateParams(params);

  params = _.extend({}, this._persistentParams || {}, params);

  params.ec = category || params.ec || this._context.ec;
  params.ea = action || params.ea || this._context.ea;
  params.el = label || params.el || this._context.el;
  params.ev = value || params.ev || this._context.ev;
  params.p = params.p || params.dp || this._context.p || this._context.dp;

  delete params.dp;
  this._tidyParameters(params);

  if (!params.ec || !params.ea) {
    return this._handleError("Please provide at least an event category (ec) and an event action (ea)", fn);
  }

  return this._withContext(params)._enqueue("event", params, fn);
}
```
- example usage
```shell
...

## Event tracking


Tracking events with 'universal-analytics' works like pageview tracking, only you have to provide different arguments:

'''javascript
visitor.event("Event Category", "Event Action").send()
'''

This is the most straightforward way to track an event. The event attributes *label* and *value* are optional and can be provided
 if necessary:

'''javascript
visitor.event("Event Category", "Event Action", "…and a label", 42).send()
'''
...
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.exception"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>exception (description, fatal, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.exception)
- description and source-code
```javascript
exception = function (description, fatal, params, fn) {

  if (typeof description === 'object') {
    params = description;
    if (typeof fatal === 'function') {
      fn = fatal;
    }
    description = fatal = null;
  } else if (typeof fatal === 'function') {
    fn = fatal;
    fatal = 0;
  } else if (typeof params === 'function') {
    fn = params;
    params = null;
  }

  params = this._translateParams(params);

  params = _.extend({}, this._persistentParams || {}, params);

  params.exd = description || params.exd || this._context.exd;
  params.exf = +!!(fatal || params.exf || this._context.exf);

  if (params.exf === 0) {
    delete params.exf;
  }

  this._tidyParameters(params);

  return this._withContext(params)._enqueue("exception", params, fn);
}
```
- example usage
```shell
...


## Exception tracking

Exception tracking is a way to keep track of any sort of application errors and bugs with Google Analytics. Using it with this module
 is a way to capture server-side problems.

'''javascript
visitor.exception("StackOverflow Error").send()
'''

As an additional information, the exception can be flagged as fatal if the error was exceptionally bad.

'''javascript
var fatal = true;
visitor.exception("StackOverflow Error", fatal, function () {
...
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.i"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>i (price, quantity, sku, name, variation, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.i)
- description and source-code
```javascript
i = function (price, quantity, sku, name, variation, params, fn) {
  if (typeof price === 'object') {
    params = price;
    if (typeof quantity === 'function') {
      fn = quantity
    }
    price = quantity = sku = name = variation = null;
  } else if (typeof quantity === 'function') {
    fn = quantity;
    quantity = sku = name = variation = null;
  } else if (typeof sku === 'function') {
    fn = sku;
    sku = name = variation = null;
  } else if (typeof name === 'function') {
    fn = name;
    name = variation = null;
  } else if (typeof variation === 'function') {
    fn = variation;
    variation = null;
  } else if (typeof params === 'function') {
    fn = params;
    params = null;
  }

  params = this._translateParams(params);

  params = _.extend({}, this._persistentParams || {}, params);

  params.ip = price || params.ip || this._context.ip;
  params.iq = quantity || params.iq || this._context.iq;
  params.ic = sku || params.ic || this._context.ic;
  params.in = name || params.in || this._context.in;
  params.iv = variation || params.iv || this._context.iv;
  params.p = params.p || this._context.p || this._context.dp;
  params.ti = params.ti || this._context.ti;

  this._tidyParameters(params);

  if (!params.ti) {
    return this._handleError("Please provide at least an item transaction ID (ti)", fn);
  }

  return this._withContext(params)._enqueue("item", params, fn);

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.item"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>item (price, quantity, sku, name, variation, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.item)
- description and source-code
```javascript
item = function (price, quantity, sku, name, variation, params, fn) {
  if (typeof price === 'object') {
    params = price;
    if (typeof quantity === 'function') {
      fn = quantity
    }
    price = quantity = sku = name = variation = null;
  } else if (typeof quantity === 'function') {
    fn = quantity;
    quantity = sku = name = variation = null;
  } else if (typeof sku === 'function') {
    fn = sku;
    sku = name = variation = null;
  } else if (typeof name === 'function') {
    fn = name;
    name = variation = null;
  } else if (typeof variation === 'function') {
    fn = variation;
    variation = null;
  } else if (typeof params === 'function') {
    fn = params;
    params = null;
  }

  params = this._translateParams(params);

  params = _.extend({}, this._persistentParams || {}, params);

  params.ip = price || params.ip || this._context.ip;
  params.iq = quantity || params.iq || this._context.iq;
  params.ic = sku || params.ic || this._context.ic;
  params.in = name || params.in || this._context.in;
  params.iv = variation || params.iv || this._context.iv;
  params.p = params.p || this._context.p || this._context.dp;
  params.ti = params.ti || this._context.ti;

  this._tidyParameters(params);

  if (!params.ti) {
    return this._handleError("Please provide at least an item transaction ID (ti)", fn);
  }

  return this._withContext(params)._enqueue("item", params, fn);

}
```
- example usage
```shell
...
## E-commerce tracking

E-commerce tracking in general is a bit more complex. It requires a combination of one call to the 'transaction()' method and one
 or more calls to the 'item()' method.

'''javascript
visitor
  .transaction("trans-12345", 500)   // Create transaction trans-12345 worth 500 total.
  .item(300, 1, "item-54321")        // Add 1 unit the item item-54321 worth 300.
  .item(200, 2, "item-41325")        // Add 2 units the item item-41325 worth 200.
  .send()
'''

Once again, daisy-chaining simplifies associating the items with the transaction. Officially, nothing but the transaction ID is
a requirement for both the transaction and the items. However, providing a minimum set of information (revenue for the transaction
, price, quantity and ID for the items) is recommended.

It is also possible to provide the params as an object to both methods:
...
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.pageview"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>pageview (path, hostname, title, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.pageview)
- description and source-code
```javascript
pageview = function (path, hostname, title, params, fn) {

  if (typeof path === 'object' && path != null) {
    params = path;
    if (typeof hostname === 'function') {
      fn = hostname
    }
    path = hostname = title  = null;
  } else if (typeof hostname === 'function') {
    fn = hostname
    hostname = title = null;
  } else if (typeof title === 'function') {
    fn = title;
    title = null;
  } else if (typeof params === 'function') {
    fn = params;
    params = null;
  }

  params = this._translateParams(params);

  params = _.extend({}, this._persistentParams || {}, params);

  params.dp = path || params.dp || this._context.dp;
  params.dh = hostname || params.dh || this._context.dh;
  params.dt = title || params.dt || this._context.dt;

  this._tidyParameters(params);

  if (!params.dp && !params.dl) {
    return this._handleError("Please provide either a page path (dp) or a document location (dl)", fn);
  }

  return this._withContext(params)._enqueue("pageview", params, fn);
}
```
- example usage
```shell
...
'''javascript
var visitor = ua('UA-XXXX-XX', {https: true});
'''

Tracking a pageview without much else is now very simple:

'''javascript
visitor.pageview("/").send()
'''

The first argument for the pageview method is the path of the page to be tracked. Simply calling 'pageview()' will not initiate
a tracking request. In order to send off tracking to the Google Analytics servers you have two options:

1. You can append a 'send()' call after 'pageview()'. The tracking request is sent asynchronously. This means you will not receive
 any confirmation when and if it was successful.
2. You can provide a callback function to 'pageview()' as an additional, last argument. This callback will be invoked once the tracking
 request has finished. Any error that occured during the request will be provided to said callback. In that case 'send()' is no
longer necessary.
...
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.pv"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>pv (path, hostname, title, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.pv)
- description and source-code
```javascript
pv = function (path, hostname, title, params, fn) {

  if (typeof path === 'object' && path != null) {
    params = path;
    if (typeof hostname === 'function') {
      fn = hostname
    }
    path = hostname = title  = null;
  } else if (typeof hostname === 'function') {
    fn = hostname
    hostname = title = null;
  } else if (typeof title === 'function') {
    fn = title;
    title = null;
  } else if (typeof params === 'function') {
    fn = params;
    params = null;
  }

  params = this._translateParams(params);

  params = _.extend({}, this._persistentParams || {}, params);

  params.dp = path || params.dp || this._context.dp;
  params.dh = hostname || params.dh || this._context.dh;
  params.dt = title || params.dt || this._context.dt;

  this._tidyParameters(params);

  if (!params.dp && !params.dl) {
    return this._handleError("Please provide either a page path (dp) or a document location (dl)", fn);
  }

  return this._withContext(params)._enqueue("pageview", params, fn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.reset"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>reset ()](#apidoc.element.universal-analytics.Visitor.prototype.reset)
- description and source-code
```javascript
reset = function () {
  this._context = null;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.screenview"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>screenview (screenName, appName, appVersion, appId, appInstallerId, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.screenview)
- description and source-code
```javascript
screenview = function (screenName, appName, appVersion, appId, appInstallerId, params, fn) {

    if (typeof screenName === 'object' && screenName != null) {
        params = screenName;
        if (typeof appName === 'function') {
            fn = appName
        }
        screenName = appName = appVersion = appId = appInstallerId = null;
    } else if (typeof appName === 'function') {
        fn = appName
        appName = appVersion = appId = appInstallerId = null;
    } else if (typeof appVersion === 'function') {
        fn = appVersion;
        appVersion = appId = appInstallerId = null;
    } else if (typeof appId === 'function') {
        fn = appId;
        appId = appInstallerId = null;
    } else if (typeof appInstallerId === 'function') {
        fn = appInstallerId;
        appInstallerId = null;
    } else if (typeof params === 'function') {
        fn = params;
        params = null;
    }

    params = this._translateParams(params);

    params = _.extend({}, this._persistentParams || {}, params);

    params.cd = screenName || params.cd || this._context.cd;
    params.an = appName || params.an || this._context.an;
    params.av = appVersion || params.av || this._context.av;
    params.aid = appId || params.aid || this._context.aid;
    params.aiid = appInstallerId || params.aiid || this._context.aiid;

    this._tidyParameters(params);

    if (!params.cd || !params.an) {
        return this._handleError("Please provide at least a screen name (cd) and an app name (an)", fn);
    }

    return this._withContext(params)._enqueue("screenview", params, fn);
}
```
- example usage
```shell
...


## Screenview tracking

Instead of pageviews app will want to track screenviews.

'''javascript
visitor.screenview("Home Screen", "App Name").send()
'''

The following method signatures are available for #screenview:

* 'Visitor#screenview(screenName, appName)'
* 'Visitor#screenview(screenName, appName, callback)'
* 'Visitor#screenview(screenName, appName, appVersion)'
...
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.send"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>send (fn)](#apidoc.element.universal-analytics.Visitor.prototype.send)
- description and source-code
```javascript
send = function (fn) {
  var self = this;
  var count = 1;
  var fn = fn || function () {};
  self._log("Sending " + self._queue.length + " tracking call(s)");

  var test = function () {
    return self._queue.length > 0;
  }

  var getBody = function(params) {
    return params.map(function(x) { return querystring.stringify(x); }).join("\n");
  }

  var iterator = function (fn) {
    var params = [];

    if(config.batching) {
      params = self._queue.splice(0, Math.min(self._queue.length, config.batchSize));
    } else {
      params.push(self._queue.shift());
    }

    var useBatchPath = params.length > 1;

    var path = config.hostname + (useBatchPath ? config.batchPath :config.path);

    self._log(count++ + ": " + JSON.stringify(params));

    var options = _.extend({}, self.options.requestOptions, {
      body: getBody(params),
      headers: self.options.headers || {}
    });

    request.post(path, options, fn);
  }

  async.whilst(test, iterator, function (err) {
    self._log("Finished sending tracking calls")
    fn.call(self, err || null, count - 1);
  });

}
```
- example usage
```shell
...
'''javascript
var visitor = ua('UA-XXXX-XX', {https: true});
'''

Tracking a pageview without much else is now very simple:

'''javascript
visitor.pageview("/").send()
'''

The first argument for the pageview method is the path of the page to be tracked. Simply calling 'pageview()' will not initiate
a tracking request. In order to send off tracking to the Google Analytics servers you have two options:

1. You can append a 'send()' call after 'pageview()'. The tracking request is sent asynchronously. This means you will not receive
 any confirmation when and if it was successful.
2. You can provide a callback function to 'pageview()' as an additional, last argument. This callback will be invoked once the tracking
 request has finished. Any error that occured during the request will be provided to said callback. In that case 'send()' is no
longer necessary.
...
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.set"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>set (key, value)](#apidoc.element.universal-analytics.Visitor.prototype.set)
- description and source-code
```javascript
set = function (key, value) {
  this._persistentParams = this._persistentParams || {};
  this._persistentParams[key] = value;
}
```
- example usage
```shell
...


# Setting persistent parameters

Some parameters should be in every tracking call, such as a user ID or custom dimensions that never or hardly change. For such situations
 a '#set(key, value)' method is available

'''javascript
  visitor.set("uid", "123456789")
'''

The uid parameter will be part of every tracking request of that visitor from now on.
...
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.t"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>t (transaction, revenue, shipping, tax, affiliation, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.t)
- description and source-code
```javascript
t = function (transaction, revenue, shipping, tax, affiliation, params, fn) {
  if (typeof transaction === 'object') {
    params = transaction;
    if (typeof revenue === 'function') {
      fn = revenue
    }
    transaction = revenue = shipping = tax = affiliation = null;
  } else if (typeof revenue === 'function') {
    fn = revenue;
    revenue = shipping = tax = affiliation = null;
  } else if (typeof shipping === 'function') {
    fn = shipping;
    shipping = tax = affiliation = null;
  } else if (typeof tax === 'function') {
    fn = tax;
    tax = affiliation = null;
  } else if (typeof affiliation === 'function') {
    fn = affiliation;
    affiliation = null;
  } else if (typeof params === 'function') {
    fn = params;
    params = null;
  }

  params = this._translateParams(params);

  params = _.extend({}, this._persistentParams || {}, params);

  params.ti = transaction || params.ti || this._context.ti;
  params.tr = revenue || params.tr || this._context.tr;
  params.ts = shipping || params.ts || this._context.ts;
  params.tt = tax || params.tt || this._context.tt;
  params.ta = affiliation || params.ta || this._context.ta;
  params.p = params.p || this._context.p || this._context.dp;

  this._tidyParameters(params);

  if (!params.ti) {
    return this._handleError("Please provide at least a transaction ID (ti)", fn);
  }

  return this._withContext(params)._enqueue("transaction", params, fn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.timing"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>timing (category, variable, time, label, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.timing)
- description and source-code
```javascript
timing = function (category, variable, time, label, params, fn) {

  if (typeof category === 'object') {
    params = category;
    if (typeof variable === 'function') {
      fn = variable;
    }
    category = variable = time = label = null;
  } else if (typeof variable === 'function') {
    fn = variable;
    variable = time = label = null;
  } else if (typeof time === 'function') {
    fn = time;
    time = label = null;
  } else if (typeof label === 'function') {
    fn = label;
    label = null;
  } else if (typeof params === 'function') {
    fn = params;
    params = null;
  }

  params = this._translateParams(params);

  params = _.extend({}, this._persistentParams || {}, params);

  params.utc = category || params.utc || this._context.utc;
  params.utv = variable || params.utv || this._context.utv;
  params.utt = time || params.utt || this._context.utt;
  params.utl = label || params.utl || this._context.utl;

  this._tidyParameters(params);

  return this._withContext(params)._enqueue("timing", params, fn);
}
```
- example usage
```shell
...


## User timing tracking

Tracking user timings is a way to capture time-based information similar to the page load speed data tracked automatically by Google
 Analytics. All arguments to this tracking method are optional, but a category, a variable and a time value should be provided.
The time value should be provided in milliseconds.

'''javascript
visitor.timing("User interaction", "Time to open login overlay", 12547).send()
'''

The following method signatures are available for #timing:

* 'Visitor#timing(category)'
* 'Visitor#timing(category, callback)'
* 'Visitor#timing(category, variable)'
...
```

#### <a name="apidoc.element.universal-analytics.Visitor.prototype.transaction"></a>[function <span class="apidocSignatureSpan">universal-analytics.Visitor.prototype.</span>transaction (transaction, revenue, shipping, tax, affiliation, params, fn)](#apidoc.element.universal-analytics.Visitor.prototype.transaction)
- description and source-code
```javascript
transaction = function (transaction, revenue, shipping, tax, affiliation, params, fn) {
  if (typeof transaction === 'object') {
    params = transaction;
    if (typeof revenue === 'function') {
      fn = revenue
    }
    transaction = revenue = shipping = tax = affiliation = null;
  } else if (typeof revenue === 'function') {
    fn = revenue;
    revenue = shipping = tax = affiliation = null;
  } else if (typeof shipping === 'function') {
    fn = shipping;
    shipping = tax = affiliation = null;
  } else if (typeof tax === 'function') {
    fn = tax;
    tax = affiliation = null;
  } else if (typeof affiliation === 'function') {
    fn = affiliation;
    affiliation = null;
  } else if (typeof params === 'function') {
    fn = params;
    params = null;
  }

  params = this._translateParams(params);

  params = _.extend({}, this._persistentParams || {}, params);

  params.ti = transaction || params.ti || this._context.ti;
  params.tr = revenue || params.tr || this._context.tr;
  params.ts = shipping || params.ts || this._context.ts;
  params.tt = tax || params.tt || this._context.tt;
  params.ta = affiliation || params.ta || this._context.ta;
  params.p = params.p || this._context.p || this._context.dp;

  this._tidyParameters(params);

  if (!params.ti) {
    return this._handleError("Please provide at least a transaction ID (ti)", fn);
  }

  return this._withContext(params)._enqueue("transaction", params, fn);
}
```
- example usage
```shell
...

## E-commerce tracking

E-commerce tracking in general is a bit more complex. It requires a combination of one call to the 'transaction()' method and one
 or more calls to the 'item()' method.

'''javascript
visitor
  .transaction("trans-12345", 500)   // Create transaction trans-12345 worth 500 total.
  .item(300, 1, "item-54321")        // Add 1 unit the item item-54321 worth 300.
  .item(200, 2, "item-41325")        // Add 2 units the item item-41325 worth 200.
  .send()
'''

Once again, daisy-chaining simplifies associating the items with the transaction. Officially, nothing but the transaction ID is
a requirement for both the transaction and the items. However, providing a minimum set of information (revenue for the transaction
, price, quantity and ID for the items) is recommended.
...
```



# <a name="apidoc.module.universal-analytics.utils"></a>[module universal-analytics.utils](#apidoc.module.universal-analytics.utils)

#### <a name="apidoc.element.universal-analytics.utils.ensureValidCid"></a>[function <span class="apidocSignatureSpan">universal-analytics.utils.</span>ensureValidCid (uuid)](#apidoc.element.universal-analytics.utils.ensureValidCid)
- description and source-code
```javascript
ensureValidCid = function (uuid) {
	if (!this.isUuid(uuid)) {
		if (!this.isCookieCid(uuid)) {
			return false;
		}
		return uuid;
	}

	uuid = uuid.replace(/\-/g, "");
	return "" +
		uuid.substring(0, 8) + "-" +
		uuid.substring(8, 12) + "-" +
		uuid.substring(12, 16) + "-" +
		uuid.substring(16, 20) + "-" +
		uuid.substring(20);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.universal-analytics.utils.isCookieCid"></a>[function <span class="apidocSignatureSpan">universal-analytics.utils.</span>isCookieCid (cid)](#apidoc.element.universal-analytics.utils.isCookieCid)
- description and source-code
```javascript
isCookieCid = function (cid) {
	return /^[0-9]+\.[0-9]+$/.test(cid)
}
```
- example usage
```shell
...
module.exports.isCookieCid = function (cid) {
	return /^[0-9]+\.[0-9]+$/.test(cid)
}


module.exports.ensureValidCid = function (uuid) {
	if (!this.isUuid(uuid)) {
		if (!this.isCookieCid(uuid)) {
			return false;
		}
		return uuid;
	}

	uuid = uuid.replace(/\-/g, "");
	return "" +
...
```

#### <a name="apidoc.element.universal-analytics.utils.isUuid"></a>[function <span class="apidocSignatureSpan">universal-analytics.utils.</span>isUuid (uuid)](#apidoc.element.universal-analytics.utils.isUuid)
- description and source-code
```javascript
isUuid = function (uuid) {
	if (!uuid) return false;
	uuid = uuid.toString().toLowerCase();
	return /[0-9a-f]{8}\-?[0-9a-f]{4}\-?4[0-9a-f]{3}\-?[89ab][0-9a-f]{3}\-?[0-9a-f]{12}/.test(uuid)
}
```
- example usage
```shell
...

module.exports.isCookieCid = function (cid) {
	return /^[0-9]+\.[0-9]+$/.test(cid)
}


module.exports.ensureValidCid = function (uuid) {
	if (!this.isUuid(uuid)) {
		if (!this.isCookieCid(uuid)) {
			return false;
		}
		return uuid;
	}

	uuid = uuid.replace(/\-/g, "");
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

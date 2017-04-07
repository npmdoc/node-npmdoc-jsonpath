# api documentation for  [jsonpath (v0.2.11)](https://github.com/dchester/jsonpath#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-jsonpath.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-jsonpath) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-jsonpath.svg)](https://travis-ci.org/npmdoc/node-npmdoc-jsonpath)
#### Query JavaScript objects with JSONPath expressions. Robust / safe JSONPath engine for Node.js.

[![NPM](https://nodei.co/npm/jsonpath.png?downloads=true)](https://www.npmjs.com/package/jsonpath)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jsonpath/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-jsonpath_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jsonpath/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-jsonpath/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-jsonpath/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "david@fmail.co.uk"
    },
    "browser": {
        "./lib/aesprim.js": "./generated/aesprim-browser.js"
    },
    "bugs": {
        "url": "https://github.com/dchester/jsonpath/issues"
    },
    "dependencies": {
        "esprima": "1.2.2",
        "jison": "0.4.13",
        "static-eval": "0.2.3",
        "underscore": "1.7.0"
    },
    "description": "Query JavaScript objects with JSONPath expressions. Robust / safe JSONPath engine for Node.js.",
    "devDependencies": {
        "grunt": "0.4.5",
        "grunt-browserify": "3.8.0",
        "grunt-cli": "0.1.13",
        "grunt-contrib-uglify": "0.9.1",
        "jscs": "1.10.0",
        "jshint": "2.6.0",
        "mocha": "2.1.0"
    },
    "directories": {},
    "dist": {
        "shasum": "bfe22e0665b9712f8e7bdf7e2e1f8c08b594c60e",
        "tarball": "https://registry.npmjs.org/jsonpath/-/jsonpath-0.2.11.tgz"
    },
    "gitHead": "4e4087c78e5d0e32a769f1270af16198bc77f2d3",
    "homepage": "https://github.com/dchester/jsonpath#readme",
    "keywords": [
        "JSONPath",
        "jsonpath",
        "json-path",
        "object",
        "traversal",
        "json",
        "path",
        "data structures"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "dchester",
            "email": "dchester@shutterstock.com"
        }
    ],
    "name": "jsonpath",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/dchester/jsonpath.git"
    },
    "scripts": {
        "generate": "node bin/generate_parser.js > generated/parser.js",
        "postinstall": "node lib/aesprim.js > generated/aesprim-browser.js",
        "test": "mocha -u tdd test && jscs lib && jshint lib"
    },
    "version": "0.2.11"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module jsonpath](#apidoc.module.jsonpath)
1.  [function <span class="apidocSignatureSpan">jsonpath.</span>JSONPath ()](#apidoc.element.jsonpath.JSONPath)
1.  [function <span class="apidocSignatureSpan">jsonpath.</span>JSONPath.Handlers ()](#apidoc.element.jsonpath.JSONPath.Handlers)
1.  object <span class="apidocSignatureSpan"></span>jsonpath
1.  object <span class="apidocSignatureSpan">jsonpath.</span>JSONPath.Handlers.prototype
1.  object <span class="apidocSignatureSpan">jsonpath.</span>JSONPath.Handlers.prototype._fns
1.  object <span class="apidocSignatureSpan">jsonpath.</span>JSONPath.prototype
1.  object <span class="apidocSignatureSpan">jsonpath.</span>aesprim
1.  object <span class="apidocSignatureSpan">jsonpath.</span>aesprim_browser
1.  object <span class="apidocSignatureSpan">jsonpath.</span>handlers
1.  object <span class="apidocSignatureSpan">jsonpath.</span>parser

#### [module jsonpath.JSONPath](#apidoc.module.jsonpath.JSONPath)
1.  [function <span class="apidocSignatureSpan">jsonpath.</span>JSONPath ()](#apidoc.element.jsonpath.JSONPath.JSONPath)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.</span>Handlers ()](#apidoc.element.jsonpath.JSONPath.Handlers)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.</span>Parser ()](#apidoc.element.jsonpath.JSONPath.Parser)

#### [module jsonpath.JSONPath.Handlers](#apidoc.module.jsonpath.JSONPath.Handlers)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.</span>Handlers ()](#apidoc.element.jsonpath.JSONPath.Handlers.Handlers)

#### [module jsonpath.JSONPath.Handlers.prototype](#apidoc.module.jsonpath.JSONPath.Handlers.prototype)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype.</span>initialize ()](#apidoc.element.jsonpath.JSONPath.Handlers.prototype.initialize)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype.</span>keys ()](#apidoc.element.jsonpath.JSONPath.Handlers.prototype.keys)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype.</span>register (key, handler)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype.register)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype.</span>resolve (component)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype.resolve)
1.  object <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype.</span>_fns

#### [module jsonpath.JSONPath.Handlers.prototype._fns](#apidoc.module.jsonpath.JSONPath.Handlers.prototype._fns)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-child-identifier (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-child-identifier)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-child-numeric_literal (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-child-numeric_literal)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-child-script_expression (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-child-script_expression)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-child-wildcard (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-child-wildcard)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-descendant-identifier (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-descendant-identifier)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-descendant-numeric_literal (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-descendant-numeric_literal)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-descendant-script_expression (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-descendant-script_expression)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-descendant-wildcard (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-descendant-wildcard)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-filter_expression (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-filter_expression)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-numeric_literal (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-numeric_literal)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-script_expression (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-script_expression)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-slice (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-slice)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-string_literal (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-string_literal)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-union (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-union)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-wildcard (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-wildcard)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-descendant-filter_expression (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-filter_expression)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-descendant-numeric_literal (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-numeric_literal)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-descendant-string_literal (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-string_literal)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-descendant-union (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-union)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-descendant-wildcard (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-wildcard)

#### [module jsonpath.JSONPath.prototype](#apidoc.module.jsonpath.JSONPath.prototype)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>_normalize (path)](#apidoc.element.jsonpath.JSONPath.prototype._normalize)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>_vivify (obj, string, value)](#apidoc.element.jsonpath.JSONPath.prototype._vivify)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>apply (obj, string, fn)](#apidoc.element.jsonpath.JSONPath.prototype.apply)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>initialize ()](#apidoc.element.jsonpath.JSONPath.prototype.initialize)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>nodes (obj, string, count)](#apidoc.element.jsonpath.JSONPath.prototype.nodes)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>parent (obj, string)](#apidoc.element.jsonpath.JSONPath.prototype.parent)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>parse (string)](#apidoc.element.jsonpath.JSONPath.prototype.parse)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>paths (obj, string, count)](#apidoc.element.jsonpath.JSONPath.prototype.paths)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>query (obj, string, count)](#apidoc.element.jsonpath.JSONPath.prototype.query)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>stringify (path)](#apidoc.element.jsonpath.JSONPath.prototype.stringify)
1.  [function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>value (obj, path, value)](#apidoc.element.jsonpath.JSONPath.prototype.value)

#### [module jsonpath.aesprim](#apidoc.module.jsonpath.aesprim)
1.  [function <span class="apidocSignatureSpan">jsonpath.aesprim.</span>parse (code, options)](#apidoc.element.jsonpath.aesprim.parse)
1.  [function <span class="apidocSignatureSpan">jsonpath.aesprim.</span>tokenize (code, options)](#apidoc.element.jsonpath.aesprim.tokenize)
1.  object <span class="apidocSignatureSpan">jsonpath.aesprim.</span>Syntax
1.  string <span class="apidocSignatureSpan">jsonpath.aesprim.</span>version

#### [module jsonpath.aesprim_browser](#apidoc.module.jsonpath.aesprim_browser)
1.  [function <span class="apidocSignatureSpan">jsonpath.aesprim_browser.</span>parse (code, options)](#apidoc.element.jsonpath.aesprim_browser.parse)
1.  [function <span class="apidocSignatureSpan">jsonpath.aesprim_browser.</span>tokenize (code, options)](#apidoc.element.jsonpath.aesprim_browser.tokenize)
1.  object <span class="apidocSignatureSpan">jsonpath.aesprim_browser.</span>Syntax
1.  string <span class="apidocSignatureSpan">jsonpath.aesprim_browser.</span>version

#### [module jsonpath.handlers](#apidoc.module.jsonpath.handlers)
1.  [function <span class="apidocSignatureSpan">jsonpath.handlers.</span>descend (partial, ref, passable, count)](#apidoc.element.jsonpath.handlers.descend)
1.  [function <span class="apidocSignatureSpan">jsonpath.handlers.</span>traverse (partial, ref, passable, count)](#apidoc.element.jsonpath.handlers.traverse)

#### [module jsonpath.jsonpath](#apidoc.module.jsonpath.jsonpath)
1.  [function <span class="apidocSignatureSpan">jsonpath.jsonpath.</span>JSONPath ()](#apidoc.element.jsonpath.jsonpath.JSONPath)
1.  object <span class="apidocSignatureSpan">jsonpath.jsonpath.</span>handlers
1.  object <span class="apidocSignatureSpan">jsonpath.jsonpath.</span>parser

#### [module jsonpath.parser](#apidoc.module.jsonpath.parser)
1.  [function <span class="apidocSignatureSpan">jsonpath.parser.</span>Parser ()](#apidoc.element.jsonpath.parser.Parser)
1.  [function <span class="apidocSignatureSpan">jsonpath.parser.</span>main (args)](#apidoc.element.jsonpath.parser.main)
1.  [function <span class="apidocSignatureSpan">jsonpath.parser.</span>parse ()](#apidoc.element.jsonpath.parser.parse)
1.  object <span class="apidocSignatureSpan">jsonpath.</span>parser



# <a name="apidoc.module.jsonpath"></a>[module jsonpath](#apidoc.module.jsonpath)

#### <a name="apidoc.element.jsonpath.JSONPath"></a>[function <span class="apidocSignatureSpan">jsonpath.</span>JSONPath ()](#apidoc.element.jsonpath.JSONPath)
- description and source-code
```javascript
JSONPath = function () {
  this.initialize.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers"></a>[function <span class="apidocSignatureSpan">jsonpath.</span>JSONPath.Handlers ()](#apidoc.element.jsonpath.JSONPath.Handlers)
- description and source-code
```javascript
JSONPath.Handlers = function () {
  return this.initialize.apply(this, arguments);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonpath.JSONPath"></a>[module jsonpath.JSONPath](#apidoc.module.jsonpath.JSONPath)

#### <a name="apidoc.element.jsonpath.JSONPath.JSONPath"></a>[function <span class="apidocSignatureSpan">jsonpath.</span>JSONPath ()](#apidoc.element.jsonpath.JSONPath.JSONPath)
- description and source-code
```javascript
JSONPath = function () {
  this.initialize.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.</span>Handlers ()](#apidoc.element.jsonpath.JSONPath.Handlers)
- description and source-code
```javascript
Handlers = function () {
  return this.initialize.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Parser"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.</span>Parser ()](#apidoc.element.jsonpath.JSONPath.Parser)
- description and source-code
```javascript
Parser = function () {

  var parser = new gparser.Parser();

  var _parseError = parser.parseError;
  parser.yy.parseError = function() {
    if (parser.yy.ast) {
      parser.yy.ast.initialize();
    }
    _parseError.apply(parser, arguments);
  }

  return parser;

}
```
- example usage
```shell
...

},{"./dict":2,"./handlers":4,"./parser":6,"assert":8}],6:[function(require,module,exports){
var grammar = require('./grammar');
var gparser = require('../generated/parser');

var Parser = function() {

var parser = new gparser.Parser();

var _parseError = parser.parseError;
parser.yy.parseError = function() {
  if (parser.yy.ast) {
    parser.yy.ast.initialize();
  }
  _parseError.apply(parser, arguments);
...
```



# <a name="apidoc.module.jsonpath.JSONPath.Handlers"></a>[module jsonpath.JSONPath.Handlers](#apidoc.module.jsonpath.JSONPath.Handlers)

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.Handlers"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.</span>Handlers ()](#apidoc.element.jsonpath.JSONPath.Handlers.Handlers)
- description and source-code
```javascript
Handlers = function () {
  return this.initialize.apply(this, arguments);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonpath.JSONPath.Handlers.prototype"></a>[module jsonpath.JSONPath.Handlers.prototype](#apidoc.module.jsonpath.JSONPath.Handlers.prototype)

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype.initialize"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype.</span>initialize ()](#apidoc.element.jsonpath.JSONPath.Handlers.prototype.initialize)
- description and source-code
```javascript
initialize = function () {
  this.traverse = traverser(true);
  this.descend = traverser();
}
```
- example usage
```shell
...
terminals_: {2:"error",4:"DOLLAR",12:"DOT",14:"DOT_DOT",15:"STAR",16:"IDENTIFIER",17:"SCRIPT_EXPRESSION",18:"INTEGER",19:"END",22
:"[",24:"]",28:",",30:"ARRAY_SLICE",31:"FILTER_EXPRESSION",32:"QQ_STRING",33:"Q_STRING"},
productions_: [0,[3,1],[3,2],[3,1],[3,2],[5,1],[5,2],[7,1],[7,1],[8,1],[8,1],[10,2],[6,1],[11,2],[13,1],[13,1],[13,1],[13,1],[13
,1],[9,1],[9,1],[20,3],[21,4],[23,1],[23,1],[26,1],[26,3],[27,1],[27,1],[27,1],[25,1],[25,1],[25,1],[29,1],[29,1]],
performAction: function anonymous(yytext, yyleng, yylineno, yy, yystate /* action[1] */, $$ /* vstack */, _$ /* lstack */
/**/) {
/* this == yyval */
if (!yy.ast) {
    yy.ast = _ast;
    _ast.initialize();
}

var $0 = $$.length - 1;
switch (yystate) {
case 1:yy.ast.set({ expression: { type: "root", value: $$[$0] } }); yy.ast.unshift(); return yy.ast.yield()
break;
case 2:yy.ast.set({ expression: { type: "root", value: $$[$0-1] } }); yy.ast.unshift(); return yy.ast.yield()
...
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype.keys"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype.</span>keys ()](#apidoc.element.jsonpath.JSONPath.Handlers.prototype.keys)
- description and source-code
```javascript
function keys() { [native code] }
```
- example usage
```shell
...
  value.forEach(function(element, index) {
    if (results.length >= count) { return }
    if (recurse) {
      descend(element, path.concat(index));
    }
  });
} else if (is_object(value)) {
  this.keys(value).forEach(function(k) {
    if (results.length >= count) { return }
    if (passable(k, value[k], ref)) {
      results.push({ path: path.concat(k), value: value[k] });
    }
  })
  this.keys(value).forEach(function(k) {
    if (results.length >= count) { return }
...
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype.register"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype.</span>register (key, handler)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype.register)
- description and source-code
```javascript
register = function (key, handler) {

  if (!handler instanceof Function) {
    throw new Error("handler must be a function");
  }

  this._fns[key] = handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype.resolve"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype.</span>resolve (component)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype.resolve)
- description and source-code
```javascript
resolve = function (component) {

  var key = [ component.operation, component.scope, component.expression.type ].join('-');
  var method = this._fns[key];

  if (!method) throw new Error("couldn't resolve key: " + key);
  return method.bind(this);
}
```
- example usage
```shell
...

        STRING_LITERAL: [
                [ 'QQ_STRING', "$$ = $1" ],
                [ 'Q_STRING',  "$$ = $1" ] ]
    }
};
if (fs.readFileSync) {
  grammar.moduleInclude = fs.readFileSync(require.resolve("../include/module.js"));
  grammar.actionInclude = fs.readFileSync(require.resolve("../include/action.js"));
}

module.exports = grammar;

},{"./dict":2,"fs":9}],4:[function(require,module,exports){
var aesprim = require('./aesprim');
...
```



# <a name="apidoc.module.jsonpath.JSONPath.Handlers.prototype._fns"></a>[module jsonpath.JSONPath.Handlers.prototype._fns](#apidoc.module.jsonpath.JSONPath.Handlers.prototype._fns)

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-child-identifier"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-child-identifier (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-child-identifier)
- description and source-code
```javascript
member-child-identifier = function (component, partial) {
  var key = component.expression.value;
  var value = partial.value;
  if (value instanceof Object && key in value) {
    return [ { value: value[key], path: partial.path.concat(key) } ]
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-child-numeric_literal"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-child-numeric_literal (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-child-numeric_literal)
- description and source-code
```javascript
member-child-numeric_literal = function (component, partial, count) {
  return this.descend(partial, component.expression.value, passable, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-child-script_expression"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-child-script_expression (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-child-script_expression)
- description and source-code
```javascript
member-child-script_expression = function (component, partial) {
  var exp = component.expression.value.slice(1, -1);
  return eval_recurse(partial, exp, '$.{{value}}');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-child-wildcard"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-child-wildcard (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-child-wildcard)
- description and source-code
```javascript
member-child-wildcard = function (component, partial, count) {
  return this.descend(partial, component.expression.value, passable, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-descendant-identifier"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-descendant-identifier (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-descendant-identifier)
- description and source-code
```javascript
member-descendant-identifier = function (component, partial, count) {
  return this.traverse(partial, component.expression.value, passable, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-descendant-numeric_literal"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-descendant-numeric_literal (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-descendant-numeric_literal)
- description and source-code
```javascript
member-descendant-numeric_literal = function (component, partial, count) {
  return this.traverse(partial, component.expression.value, passable, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-descendant-script_expression"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-descendant-script_expression (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-descendant-script_expression)
- description and source-code
```javascript
member-descendant-script_expression = function (component, partial) {
  var exp = component.expression.value.slice(1, -1);
  return eval_recurse(partial, exp, '$..value');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-descendant-wildcard"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>member-descendant-wildcard (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.member-descendant-wildcard)
- description and source-code
```javascript
member-descendant-wildcard = function (component, partial, count) {
  return this.traverse(partial, component.expression.value, passable, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-filter_expression"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-filter_expression (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-filter_expression)
- description and source-code
```javascript
subscript-child-filter_expression = function (component, partial, count) {

  // slice out the expression from ?(expression)
  var src = component.expression.value.slice(2, -1);
  var ast = aesprim.parse(src).body[0].expression;

  var passable = function(key, value) {
    return evaluate(ast, { '@': value });
  }

  return this.descend(partial, null, passable, count);

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-numeric_literal"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-numeric_literal (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-numeric_literal)
- description and source-code
```javascript
subscript-child-numeric_literal = function (component, partial, count) {
  return this.descend(partial, component.expression.value, passable, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-script_expression"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-script_expression (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-script_expression)
- description and source-code
```javascript
subscript-child-script_expression = function (component, partial) {
  var exp = component.expression.value.slice(1, -1);
  return eval_recurse(partial, exp, '$[{{value}}]');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-slice"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-slice (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-slice)
- description and source-code
```javascript
subscript-child-slice = function (component, partial) {
  if (is_array(partial.value)) {
    var args = component.expression.value.split(':').map(_parse_nullable_int);
    var values = partial.value.map(function(v, i) { return { value: v, path: partial.path.concat(i) } });
    return slice.apply(null, [values].concat(args));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-string_literal"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-string_literal (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-string_literal)
- description and source-code
```javascript
subscript-child-string_literal = function (component, partial) {
  var key = component.expression.value;
  var value = partial.value;
  if (value instanceof Object && key in value) {
    return [ { value: value[key], path: partial.path.concat(key) } ]
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-union"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-union (component, partial)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-union)
- description and source-code
```javascript
subscript-child-union = function (component, partial) {
  var results = [];
  component.expression.value.forEach(function(component) {
    var _component = { operation: 'subscript', scope: 'child', expression: component.expression };
    var handler = this.resolve(_component);
    var _results = handler(_component, partial);
    if (_results) {
      results = results.concat(_results);
    }
  }, this);

  return unique(results);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-wildcard"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-child-wildcard (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-child-wildcard)
- description and source-code
```javascript
subscript-child-wildcard = function (component, partial, count) {
  return this.descend(partial, component.expression.value, passable, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-filter_expression"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-descendant-filter_expression (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-filter_expression)
- description and source-code
```javascript
subscript-descendant-filter_expression = function (component, partial, count) {

  // slice out the expression from ?(expression)
  var src = component.expression.value.slice(2, -1);
  var ast = aesprim.parse(src).body[0].expression;

  var passable = function(key, value) {
    return evaluate(ast, { '@': value });
  }

  return this.traverse(partial, null, passable, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-numeric_literal"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-descendant-numeric_literal (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-numeric_literal)
- description and source-code
```javascript
subscript-descendant-numeric_literal = function (component, partial, count) {
  return this.traverse(partial, component.expression.value, passable, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-string_literal"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-descendant-string_literal (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-string_literal)
- description and source-code
```javascript
subscript-descendant-string_literal = function (component, partial, count) {
  return this.traverse(partial, component.expression.value, passable, count);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-union"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-descendant-union (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-union)
- description and source-code
```javascript
subscript-descendant-union = function (component, partial, count) {

  var jp = require('..');
  var self = this;

  var results = [];
  var nodes = jp.nodes(partial, '$..*').slice(1);

  nodes.forEach(function(node) {
    if (results.length >= count) return;
    component.expression.value.forEach(function(component) {
      var _component = { operation: 'subscript', scope: 'child', expression: component.expression };
      var handler = self.resolve(_component);
      var _results = handler(_component, node);
      results = results.concat(_results);
    });
  });

  return unique(results);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-wildcard"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.Handlers.prototype._fns.</span>subscript-descendant-wildcard (component, partial, count)](#apidoc.element.jsonpath.JSONPath.Handlers.prototype._fns.subscript-descendant-wildcard)
- description and source-code
```javascript
subscript-descendant-wildcard = function (component, partial, count) {
  return this.traverse(partial, component.expression.value, passable, count);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonpath.JSONPath.prototype"></a>[module jsonpath.JSONPath.prototype](#apidoc.module.jsonpath.JSONPath.prototype)

#### <a name="apidoc.element.jsonpath.JSONPath.prototype._normalize"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>_normalize (path)](#apidoc.element.jsonpath.JSONPath.prototype._normalize)
- description and source-code
```javascript
_normalize = function (path) {

  assert.ok(path, "we need a path");

  if (typeof path == "string") {

    return this.parser.parse(path);

  } else if (Array.isArray(path) && typeof path[0] == "string") {

    var _path = [ { expression: { type: "root", value: "$" } } ];

    path.forEach(function(component, index) {

      if (component == '$' && index === 0) return;

      if (typeof component == "string" && component.match("^" + dict.identifier + "$")) {

        _path.push({
          operation: 'member',
          scope: 'child',
          expression: { value: component, type: 'identifier' }
        });

      } else {

        var type = typeof component == "number" ?
          'numeric_literal' : 'string_literal';

        _path.push({
          operation: 'subscript',
          scope: 'child',
          expression: { value: component, type: type }
        });
      }
    });

    return _path;

  } else if (Array.isArray(path) && typeof path[0] == "object") {

    return path
  }

  throw new Error("couldn't understand path " + path);
}
```
- example usage
```shell
...
  var templates = {
'descendant-member': '..{{value}}',
'child-member': '.{{value}}',
'descendant-subscript': '..[{{value}}]',
'child-subscript': '[{{value}}]'
  };

  path = this._normalize(path);

  path.forEach(function(component) {

if (component.expression.type == 'root') return;

var key = [component.scope, component.operation].join('-');
var template = templates[key];
...
```

#### <a name="apidoc.element.jsonpath.JSONPath.prototype._vivify"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>_vivify (obj, string, value)](#apidoc.element.jsonpath.JSONPath.prototype._vivify)
- description and source-code
```javascript
_vivify = function (obj, string, value) {

  var self = this;

  assert.ok(obj instanceof Object, "obj needs to be an object");
  assert.ok(string, "we need a path");

  var path = this.parser.parse(string)
    .map(function(component) { return component.expression.value });

  var setValue = function(path, value) {
    var key = path.pop();
    var node = self.value(obj, path);
    if (!node) {
      setValue(path.concat(), typeof key === 'string' ? {} : []);
      node = self.value(obj, path);
    }
    node[key] = value;
  }
  setValue(path, value);
  return this.query(obj, string)[0];
}
```
- example usage
```shell
...
JSONPath.prototype.value = function(obj, path, value) {

  assert.ok(obj instanceof Object, "obj needs to be an object");
  assert.ok(path, "we need a path");

  if (arguments.length >= 3) {
    var node = this.nodes(obj, path).shift();
    if (!node) return this._vivify(obj, path, value);
    var key = node.path.slice(-1).shift();
    var parent = this.parent(obj, this.stringify(node.path));
    parent[key] = value;
  }
  return this.query(obj, this.stringify(path), 1).shift();
}
...
```

#### <a name="apidoc.element.jsonpath.JSONPath.prototype.apply"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>apply (obj, string, fn)](#apidoc.element.jsonpath.JSONPath.prototype.apply)
- description and source-code
```javascript
apply = function (obj, string, fn) {

  assert.ok(obj instanceof Object, "obj needs to be an object");
  assert.ok(string, "we need a path");
  assert.equal(typeof fn, "function", "fn needs to be function")

  var nodes = this.nodes(obj, string).sort(function(a, b) {
    // sort nodes so we apply from the bottom up
    return b.path.length - a.path.length;
  });

  nodes.forEach(function(node) {
    var key = node.path.pop();
    var parent = this.value(obj, this.stringify(node.path));
    var val = node.value = fn.call(obj, parent[key]);
    parent[key] = val;
  }, this);

  return nodes;
}
```
- example usage
```shell
...

Returns the value of the first element matching 'pathExpression'.  If 'newValue' is provided, sets the value of the first matching
 element and returns the new value.

#### jp.parent(obj, pathExpression)

Returns the parent of the first matching element.

#### jp.apply(obj, pathExpression, fn)

Runs the supplied function 'fn' on each matching element, and replaces each matching element with the return value from the function
.  The function accepts the value of the matching element as its only parameter.  Returns matching nodes with their updated values
.


'''javascript
var nodes = jp.apply(data, '$..author', function(value) { return value.toUpperCase() });
// [
...
```

#### <a name="apidoc.element.jsonpath.JSONPath.prototype.initialize"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>initialize ()](#apidoc.element.jsonpath.JSONPath.prototype.initialize)
- description and source-code
```javascript
initialize = function () {
  this.parser = new Parser();
  this.handlers = new Handlers();
}
```
- example usage
```shell
...
terminals_: {2:"error",4:"DOLLAR",12:"DOT",14:"DOT_DOT",15:"STAR",16:"IDENTIFIER",17:"SCRIPT_EXPRESSION",18:"INTEGER",19:"END",22
:"[",24:"]",28:",",30:"ARRAY_SLICE",31:"FILTER_EXPRESSION",32:"QQ_STRING",33:"Q_STRING"},
productions_: [0,[3,1],[3,2],[3,1],[3,2],[5,1],[5,2],[7,1],[7,1],[8,1],[8,1],[10,2],[6,1],[11,2],[13,1],[13,1],[13,1],[13,1],[13
,1],[9,1],[9,1],[20,3],[21,4],[23,1],[23,1],[26,1],[26,3],[27,1],[27,1],[27,1],[25,1],[25,1],[25,1],[29,1],[29,1]],
performAction: function anonymous(yytext, yyleng, yylineno, yy, yystate /* action[1] */, $$ /* vstack */, _$ /* lstack */
/**/) {
/* this == yyval */
if (!yy.ast) {
    yy.ast = _ast;
    _ast.initialize();
}

var $0 = $$.length - 1;
switch (yystate) {
case 1:yy.ast.set({ expression: { type: "root", value: $$[$0] } }); yy.ast.unshift(); return yy.ast.yield()
break;
case 2:yy.ast.set({ expression: { type: "root", value: $$[$0-1] } }); yy.ast.unshift(); return yy.ast.yield()
...
```

#### <a name="apidoc.element.jsonpath.JSONPath.prototype.nodes"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>nodes (obj, string, count)](#apidoc.element.jsonpath.JSONPath.prototype.nodes)
- description and source-code
```javascript
nodes = function (obj, string, count) {

  assert.ok(obj instanceof Object, "obj needs to be an object");
  assert.ok(string, "we need a path");

  if (count === 0) return [];

  var path = this.parser.parse(string);
  var handlers = this.handlers;

  var partials = [ { path: ['$'], value: obj } ];
  var matches = [];

  if (path.length && path[0].expression.type == 'root') path.shift();

  if (!path.length) return partials;

  path.forEach(function(component, index) {

    if (matches.length >= count) return;
    var handler = handlers.resolve(component);
    var _partials = [];

    partials.forEach(function(p) {

      if (matches.length >= count) return;
      var results = handler(component, p, count);

      if (index == path.length - 1) {
        // if we're through the components we're done
        matches = matches.concat(results || []);
      } else {
        // otherwise accumulate and carry on through
        _partials = _partials.concat(results || []);
      }
    });

    partials = _partials;

  });

  return count ? matches.slice(0, count) : matches;
}
```
- example usage
```shell
...
//   ['$', 'store', 'book', 0, 'author'] },
//   ['$', 'store', 'book', 1, 'author'] },
//   ['$', 'store', 'book', 2, 'author'] },
//   ['$', 'store', 'book', 3, 'author'] }
// ]
'''

#### jp.nodes(obj, pathExpression[, count])

Find elements and their corresponding paths in 'obj' matching 'pathExpression'.  Returns an array of node objects where each node
 has a 'path' containing an array of keys representing the location within 'obj', and a 'value' pointing to the matched element.
Returns only first 'count' nodes if specified.

'''javascript
var nodes = jp.nodes(data, '$..author');
// [
//   { path: ['$', 'store', 'book', 0, 'author'], value: 'Nigel Rees' },
...
```

#### <a name="apidoc.element.jsonpath.JSONPath.prototype.parent"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>parent (obj, string)](#apidoc.element.jsonpath.JSONPath.prototype.parent)
- description and source-code
```javascript
parent = function (obj, string) {

  assert.ok(obj instanceof Object, "obj needs to be an object");
  assert.ok(string, "we need a path");

  var node = this.nodes(obj, string)[0];
  var key = node.path.pop();<span class="apidocCodeCommentSpan"> /* jshint unused:false */
</span>  return this.value(obj, node.path);
}
```
- example usage
```shell
...
// ]
'''

#### jp.value(obj, pathExpression[, newValue])

Returns the value of the first element matching 'pathExpression'.  If 'newValue' is provided, sets the value of the first matching
 element and returns the new value.

#### jp.parent(obj, pathExpression)

Returns the parent of the first matching element.

#### jp.apply(obj, pathExpression, fn)

Runs the supplied function 'fn' on each matching element, and replaces each matching element with the return value from the function
.  The function accepts the value of the matching element as its only parameter.  Returns matching nodes with their updated values
.
...
```

#### <a name="apidoc.element.jsonpath.JSONPath.prototype.parse"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>parse (string)](#apidoc.element.jsonpath.JSONPath.prototype.parse)
- description and source-code
```javascript
parse = function (string) {
  assert.ok(_is_string(string), "we need a path");
  return this.parser.parse(string);
}
```
- example usage
```shell
...
//   { path: ['$', 'store', 'book', 0, 'author'], value: 'NIGEL REES' },
//   { path: ['$', 'store', 'book', 1, 'author'], value: 'EVELYN WAUGH' },
//   { path: ['$', 'store', 'book', 2, 'author'], value: 'HERMAN MELVILLE' },
//   { path: ['$', 'store', 'book', 3, 'author'], value: 'J. R. R. TOLKIEN' }
// ]
'''

#### jp.parse(pathExpression)

Parse the provided JSONPath expression into path components and their associated operations.

'''javascript
var path = jp.parse('$..author');
// [
//   { expression: { type: 'root', value: '$' } },
...
```

#### <a name="apidoc.element.jsonpath.JSONPath.prototype.paths"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>paths (obj, string, count)](#apidoc.element.jsonpath.JSONPath.prototype.paths)
- description and source-code
```javascript
paths = function (obj, string, count) {

  assert.ok(obj instanceof Object, "obj needs to be an object");
  assert.ok(string, "we need a path");

  var results = this.nodes(obj, string, count)
    .map(function(r) { return r.path });

  return results;
}
```
- example usage
```shell
...
Find elements in 'obj' matching 'pathExpression'.  Returns an array of elements that satisfy the provided JSONPath expression, or
 an empty array if none were matched.  Returns only first 'count' elements if specified.

'''javascript
var authors = jp.query(data, '$..author');
// [ 'Nigel Rees', 'Evelyn Waugh', 'Herman Melville', 'J. R. R. Tolkien' ]
'''

#### jp.paths(obj, pathExpression[, count])

Find paths to elements in 'obj' matching 'pathExpression'.  Returns an array of element paths that satisfy the provided JSONPath
 expression. Each path is itself an array of keys representing the location within 'obj' of the matching element.  Returns only
first 'count' paths if specified.


'''javascript
var paths = jp.paths(data, '$..author');
// [
...
```

#### <a name="apidoc.element.jsonpath.JSONPath.prototype.query"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>query (obj, string, count)](#apidoc.element.jsonpath.JSONPath.prototype.query)
- description and source-code
```javascript
query = function (obj, string, count) {

  assert.ok(obj instanceof Object, "obj needs to be an object");
  assert.ok(_is_string(string), "we need a path");

  var results = this.nodes(obj, string, count)
    .map(function(r) { return r.value });

  return results;
}
```
- example usage
```shell
...
  { name: "London", "population": 8615246 },
  { name: "Berlin", "population": 3517424 },
  { name: "Madrid", "population": 3165235 },
  { name: "Rome",   "population": 2870528 }
];

var jp = require('jsonpath');
var names = jp.query(cities, '$..name');

// [ "London", "Berlin", "Madrid", "Rome" ]
'''

## Install

Install from npm:
...
```

#### <a name="apidoc.element.jsonpath.JSONPath.prototype.stringify"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>stringify (path)](#apidoc.element.jsonpath.JSONPath.prototype.stringify)
- description and source-code
```javascript
stringify = function (path) {

  assert.ok(path, "we need a path");

  var string = '$';

  var templates = {
    'descendant-member': '..{{value}}',
    'child-member': '.{{value}}',
    'descendant-subscript': '..[{{value}}]',
    'child-subscript': '[{{value}}]'
  };

  path = this._normalize(path);

  path.forEach(function(component) {

    if (component.expression.type == 'root') return;

    var key = [component.scope, component.operation].join('-');
    var template = templates[key];
    var value;

    if (component.expression.type == 'string_literal') {
      value = JSON.stringify(component.expression.value)
    } else {
      value = component.expression.value;
    }

    if (!template) throw new Error("couldn't find template " + key);

    string += template.replace(/{{value}}/, value);
  });

  return string;
}
```
- example usage
```shell
...
var path = jp.parse('$..author');
// [
//   { expression: { type: 'root', value: '$' } },
//   { expression: { type: 'identifier', value: 'author' }, operation: 'member', scope: 'descendant' }
// ]
'''

#### jp.stringify(path)

Returns a path expression in string form, given a path.  The supplied path may either be a flat array of keys, as returned by 'jp
.nodes' for example, or may alternatively be a fully parsed path expression in the form of an array of path components as returned
 by 'jp.parse'.

'''javascript
var pathExpression = jp.stringify(['$', 'store', 'book', 0, 'author']);
// "$.store.book[0].author"
'''
...
```

#### <a name="apidoc.element.jsonpath.JSONPath.prototype.value"></a>[function <span class="apidocSignatureSpan">jsonpath.JSONPath.prototype.</span>value (obj, path, value)](#apidoc.element.jsonpath.JSONPath.prototype.value)
- description and source-code
```javascript
value = function (obj, path, value) {

  assert.ok(obj instanceof Object, "obj needs to be an object");
  assert.ok(path, "we need a path");

  if (arguments.length >= 3) {
    var node = this.nodes(obj, path).shift();
    if (!node) return this._vivify(obj, path, value);
    var key = node.path.slice(-1).shift();
    var parent = this.parent(obj, this.stringify(node.path));
    parent[key] = value;
  }
  return this.query(obj, this.stringify(path), 1).shift();
}
```
- example usage
```shell
...
//   { path: ['$', 'store', 'book', 0, 'author'], value: 'Nigel Rees' },
//   { path: ['$', 'store', 'book', 1, 'author'], value: 'Evelyn Waugh' },
//   { path: ['$', 'store', 'book', 2, 'author'], value: 'Herman Melville' },
//   { path: ['$', 'store', 'book', 3, 'author'], value: 'J. R. R. Tolkien' }
// ]
'''

#### jp.value(obj, pathExpression[, newValue])

Returns the value of the first element matching 'pathExpression'.  If 'newValue' is provided, sets the value of the first matching
 element and returns the new value.

#### jp.parent(obj, pathExpression)

Returns the parent of the first matching element.
...
```



# <a name="apidoc.module.jsonpath.aesprim"></a>[module jsonpath.aesprim](#apidoc.module.jsonpath.aesprim)

#### <a name="apidoc.element.jsonpath.aesprim.parse"></a>[function <span class="apidocSignatureSpan">jsonpath.aesprim.</span>parse (code, options)](#apidoc.element.jsonpath.aesprim.parse)
- description and source-code
```javascript
function parse(code, options) {
    var program, toString;

    toString = String;
    if (typeof code !== 'string' && !(code instanceof String)) {
        code = toString(code);
    }

    delegate = SyntaxTreeDelegate;
    source = code;
    index = 0;
    lineNumber = (source.length > 0) ? 1 : 0;
    lineStart = 0;
    length = source.length;
    lookahead = null;
    state = {
        allowIn: true,
        labelSet: {},
        inFunctionBody: false,
        inIteration: false,
        inSwitch: false,
        lastCommentStart: -1
    };

    extra = {};
    if (typeof options !== 'undefined') {
        extra.range = (typeof options.range === 'boolean') && options.range;
        extra.loc = (typeof options.loc === 'boolean') && options.loc;
        extra.attachComment = (typeof options.attachComment === 'boolean') && options.attachComment;

        if (extra.loc && options.source !== null && options.source !== undefined) {
            extra.source = toString(options.source);
        }

        if (typeof options.tokens === 'boolean' && options.tokens) {
            extra.tokens = [];
        }
        if (typeof options.comment === 'boolean' && options.comment) {
            extra.comments = [];
        }
        if (typeof options.tolerant === 'boolean' && options.tolerant) {
            extra.errors = [];
        }
        if (extra.attachComment) {
            extra.range = true;
            extra.comments = [];
            extra.bottomRightStack = [];
            extra.trailingComments = [];
            extra.leadingComments = [];
        }
    }

    try {
        program = parseProgram();
        if (typeof extra.comments !== 'undefined') {
            program.comments = extra.comments;
        }
        if (typeof extra.tokens !== 'undefined') {
            filterTokenLocation();
            program.tokens = extra.tokens;
        }
        if (typeof extra.errors !== 'undefined') {
            program.errors = extra.errors;
        }
    } catch (e) {
        throw e;
    } finally {
        extra = {};
    }

    return program;
}
```
- example usage
```shell
...
//   { path: ['$', 'store', 'book', 0, 'author'], value: 'NIGEL REES' },
//   { path: ['$', 'store', 'book', 1, 'author'], value: 'EVELYN WAUGH' },
//   { path: ['$', 'store', 'book', 2, 'author'], value: 'HERMAN MELVILLE' },
//   { path: ['$', 'store', 'book', 3, 'author'], value: 'J. R. R. TOLKIEN' }
// ]
'''

#### jp.parse(pathExpression)

Parse the provided JSONPath expression into path components and their associated operations.

'''javascript
var path = jp.parse('$..author');
// [
//   { expression: { type: 'root', value: '$' } },
...
```

#### <a name="apidoc.element.jsonpath.aesprim.tokenize"></a>[function <span class="apidocSignatureSpan">jsonpath.aesprim.</span>tokenize (code, options)](#apidoc.element.jsonpath.aesprim.tokenize)
- description and source-code
```javascript
function tokenize(code, options) {
    var toString,
        token,
        tokens;

    toString = String;
    if (typeof code !== 'string' && !(code instanceof String)) {
        code = toString(code);
    }

    delegate = SyntaxTreeDelegate;
    source = code;
    index = 0;
    lineNumber = (source.length > 0) ? 1 : 0;
    lineStart = 0;
    length = source.length;
    lookahead = null;
    state = {
        allowIn: true,
        labelSet: {},
        inFunctionBody: false,
        inIteration: false,
        inSwitch: false,
        lastCommentStart: -1
    };

    extra = {};

    // Options matching.
    options = options || {};

    // Of course we collect tokens here.
    options.tokens = true;
    extra.tokens = [];
    extra.tokenize = true;
    // The following two fields are necessary to compute the Regex tokens.
    extra.openParenToken = -1;
    extra.openCurlyToken = -1;

    extra.range = (typeof options.range === 'boolean') && options.range;
    extra.loc = (typeof options.loc === 'boolean') && options.loc;

    if (typeof options.comment === 'boolean' && options.comment) {
        extra.comments = [];
    }
    if (typeof options.tolerant === 'boolean' && options.tolerant) {
        extra.errors = [];
    }

    try {
        peek();
        if (lookahead.type === Token.EOF) {
            return extra.tokens;
        }

        token = lex();
        while (lookahead.type !== Token.EOF) {
            try {
                token = lex();
            } catch (lexError) {
                token = lookahead;
                if (extra.errors) {
                    extra.errors.push(lexError);
                    // We have to break on the first error
                    // to avoid infinite loops.
                    break;
                } else {
                    throw lexError;
                }
            }
        }

        filterTokenLocation();
        tokens = extra.tokens;
        if (typeof extra.comments !== 'undefined') {
            tokens.comments = extra.comments;
        }
        if (typeof extra.errors !== 'undefined') {
            tokens.errors = extra.errors;
        }
    } catch (e) {
        throw e;
    } finally {
        extra = {};
    }
    return tokens;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonpath.aesprim_browser"></a>[module jsonpath.aesprim_browser](#apidoc.module.jsonpath.aesprim_browser)

#### <a name="apidoc.element.jsonpath.aesprim_browser.parse"></a>[function <span class="apidocSignatureSpan">jsonpath.aesprim_browser.</span>parse (code, options)](#apidoc.element.jsonpath.aesprim_browser.parse)
- description and source-code
```javascript
function parse(code, options) {
    var program, toString;

    toString = String;
    if (typeof code !== 'string' && !(code instanceof String)) {
        code = toString(code);
    }

    delegate = SyntaxTreeDelegate;
    source = code;
    index = 0;
    lineNumber = (source.length > 0) ? 1 : 0;
    lineStart = 0;
    length = source.length;
    lookahead = null;
    state = {
        allowIn: true,
        labelSet: {},
        inFunctionBody: false,
        inIteration: false,
        inSwitch: false,
        lastCommentStart: -1
    };

    extra = {};
    if (typeof options !== 'undefined') {
        extra.range = (typeof options.range === 'boolean') && options.range;
        extra.loc = (typeof options.loc === 'boolean') && options.loc;
        extra.attachComment = (typeof options.attachComment === 'boolean') && options.attachComment;

        if (extra.loc && options.source !== null && options.source !== undefined) {
            extra.source = toString(options.source);
        }

        if (typeof options.tokens === 'boolean' && options.tokens) {
            extra.tokens = [];
        }
        if (typeof options.comment === 'boolean' && options.comment) {
            extra.comments = [];
        }
        if (typeof options.tolerant === 'boolean' && options.tolerant) {
            extra.errors = [];
        }
        if (extra.attachComment) {
            extra.range = true;
            extra.comments = [];
            extra.bottomRightStack = [];
            extra.trailingComments = [];
            extra.leadingComments = [];
        }
    }

    try {
        program = parseProgram();
        if (typeof extra.comments !== 'undefined') {
            program.comments = extra.comments;
        }
        if (typeof extra.tokens !== 'undefined') {
            filterTokenLocation();
            program.tokens = extra.tokens;
        }
        if (typeof extra.errors !== 'undefined') {
            program.errors = extra.errors;
        }
    } catch (e) {
        throw e;
    } finally {
        extra = {};
    }

    return program;
}
```
- example usage
```shell
...
//   { path: ['$', 'store', 'book', 0, 'author'], value: 'NIGEL REES' },
//   { path: ['$', 'store', 'book', 1, 'author'], value: 'EVELYN WAUGH' },
//   { path: ['$', 'store', 'book', 2, 'author'], value: 'HERMAN MELVILLE' },
//   { path: ['$', 'store', 'book', 3, 'author'], value: 'J. R. R. TOLKIEN' }
// ]
'''

#### jp.parse(pathExpression)

Parse the provided JSONPath expression into path components and their associated operations.

'''javascript
var path = jp.parse('$..author');
// [
//   { expression: { type: 'root', value: '$' } },
...
```

#### <a name="apidoc.element.jsonpath.aesprim_browser.tokenize"></a>[function <span class="apidocSignatureSpan">jsonpath.aesprim_browser.</span>tokenize (code, options)](#apidoc.element.jsonpath.aesprim_browser.tokenize)
- description and source-code
```javascript
function tokenize(code, options) {
    var toString,
        token,
        tokens;

    toString = String;
    if (typeof code !== 'string' && !(code instanceof String)) {
        code = toString(code);
    }

    delegate = SyntaxTreeDelegate;
    source = code;
    index = 0;
    lineNumber = (source.length > 0) ? 1 : 0;
    lineStart = 0;
    length = source.length;
    lookahead = null;
    state = {
        allowIn: true,
        labelSet: {},
        inFunctionBody: false,
        inIteration: false,
        inSwitch: false,
        lastCommentStart: -1
    };

    extra = {};

    // Options matching.
    options = options || {};

    // Of course we collect tokens here.
    options.tokens = true;
    extra.tokens = [];
    extra.tokenize = true;
    // The following two fields are necessary to compute the Regex tokens.
    extra.openParenToken = -1;
    extra.openCurlyToken = -1;

    extra.range = (typeof options.range === 'boolean') && options.range;
    extra.loc = (typeof options.loc === 'boolean') && options.loc;

    if (typeof options.comment === 'boolean' && options.comment) {
        extra.comments = [];
    }
    if (typeof options.tolerant === 'boolean' && options.tolerant) {
        extra.errors = [];
    }

    try {
        peek();
        if (lookahead.type === Token.EOF) {
            return extra.tokens;
        }

        token = lex();
        while (lookahead.type !== Token.EOF) {
            try {
                token = lex();
            } catch (lexError) {
                token = lookahead;
                if (extra.errors) {
                    extra.errors.push(lexError);
                    // We have to break on the first error
                    // to avoid infinite loops.
                    break;
                } else {
                    throw lexError;
                }
            }
        }

        filterTokenLocation();
        tokens = extra.tokens;
        if (typeof extra.comments !== 'undefined') {
            tokens.comments = extra.comments;
        }
        if (typeof extra.errors !== 'undefined') {
            tokens.errors = extra.errors;
        }
    } catch (e) {
        throw e;
    } finally {
        extra = {};
    }
    return tokens;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonpath.handlers"></a>[module jsonpath.handlers](#apidoc.module.jsonpath.handlers)

#### <a name="apidoc.element.jsonpath.handlers.descend"></a>[function <span class="apidocSignatureSpan">jsonpath.handlers.</span>descend (partial, ref, passable, count)](#apidoc.element.jsonpath.handlers.descend)
- description and source-code
```javascript
descend = function (partial, ref, passable, count) {

  var value = partial.value;
  var path = partial.path;

  var results = [];

  var descend = function(value, path) {

    if (is_array(value)) {
      value.forEach(function(element, index) {
        if (results.length >= count) { return }
        if (passable(index, element, ref)) {
          results.push({ path: path.concat(index), value: element });
        }
      });
      value.forEach(function(element, index) {
        if (results.length >= count) { return }
        if (recurse) {
          descend(element, path.concat(index));
        }
      });
    } else if (is_object(value)) {
      this.keys(value).forEach(function(k) {
        if (results.length >= count) { return }
        if (passable(k, value[k], ref)) {
          results.push({ path: path.concat(k), value: value[k] });
        }
      })
      this.keys(value).forEach(function(k) {
        if (results.length >= count) { return }
        if (recurse) {
          descend(value[k], path.concat(k));
        }
      });
    }
  }.bind(this);
  descend(value, path);
  return results;
}
```
- example usage
```shell
...
var src = component.expression.value.slice(2, -1);
var ast = aesprim.parse(src).body[0].expression;

var passable = function(key, value) {
  return evaluate(ast, { '@': value });
}

return this.descend(partial, null, passable, count);

  },

  'subscript-descendant-filter_expression': function(component, partial, count) {

// slice out the expression from ?(expression)
var src = component.expression.value.slice(2, -1);
...
```

#### <a name="apidoc.element.jsonpath.handlers.traverse"></a>[function <span class="apidocSignatureSpan">jsonpath.handlers.</span>traverse (partial, ref, passable, count)](#apidoc.element.jsonpath.handlers.traverse)
- description and source-code
```javascript
traverse = function (partial, ref, passable, count) {

  var value = partial.value;
  var path = partial.path;

  var results = [];

  var descend = function(value, path) {

    if (is_array(value)) {
      value.forEach(function(element, index) {
        if (results.length >= count) { return }
        if (passable(index, element, ref)) {
          results.push({ path: path.concat(index), value: element });
        }
      });
      value.forEach(function(element, index) {
        if (results.length >= count) { return }
        if (recurse) {
          descend(element, path.concat(index));
        }
      });
    } else if (is_object(value)) {
      this.keys(value).forEach(function(k) {
        if (results.length >= count) { return }
        if (passable(k, value[k], ref)) {
          results.push({ path: path.concat(k), value: value[k] });
        }
      })
      this.keys(value).forEach(function(k) {
        if (results.length >= count) { return }
        if (recurse) {
          descend(value[k], path.concat(k));
        }
      });
    }
  }.bind(this);
  descend(value, path);
  return results;
}
```
- example usage
```shell
...
  var src = component.expression.value.slice(2, -1);
  var ast = aesprim.parse(src).body[0].expression;

  var passable = function(key, value) {
    return evaluate(ast, { '@': value });
  }

  return this.traverse(partial, null, passable, count);
},

'subscript-child-script_expression': function(component, partial) {
  var exp = component.expression.value.slice(1, -1);
  return eval_recurse(partial, exp, '$[{{value}}]');
},
...
```



# <a name="apidoc.module.jsonpath.jsonpath"></a>[module jsonpath.jsonpath](#apidoc.module.jsonpath.jsonpath)

#### <a name="apidoc.element.jsonpath.jsonpath.JSONPath"></a>[function <span class="apidocSignatureSpan">jsonpath.jsonpath.</span>JSONPath ()](#apidoc.element.jsonpath.jsonpath.JSONPath)
- description and source-code
```javascript
JSONPath = function () {
  this.initialize.apply(this, arguments);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonpath.parser"></a>[module jsonpath.parser](#apidoc.module.jsonpath.parser)

#### <a name="apidoc.element.jsonpath.parser.Parser"></a>[function <span class="apidocSignatureSpan">jsonpath.parser.</span>Parser ()](#apidoc.element.jsonpath.parser.Parser)
- description and source-code
```javascript
function Parser() {
  this.yy = {};
}
```
- example usage
```shell
...

},{"./dict":2,"./handlers":4,"./parser":6,"assert":8}],6:[function(require,module,exports){
var grammar = require('./grammar');
var gparser = require('../generated/parser');

var Parser = function() {

var parser = new gparser.Parser();

var _parseError = parser.parseError;
parser.yy.parseError = function() {
  if (parser.yy.ast) {
    parser.yy.ast.initialize();
  }
  _parseError.apply(parser, arguments);
...
```

#### <a name="apidoc.element.jsonpath.parser.main"></a>[function <span class="apidocSignatureSpan">jsonpath.parser.</span>main (args)](#apidoc.element.jsonpath.parser.main)
- description and source-code
```javascript
function commonjsMain(args) {
    if (!args[1]) {
        console.log('Usage: '+args[0]+' FILE');
        process.exit(1);
    }
    var source = require('fs').readFileSync(require('path').normalize(args[1]), "utf8");
    return exports.parser.parse(source);
}
```
- example usage
```shell
...
        console.log('Usage: '+args[0]+' FILE');
        process.exit(1);
    }
    var source = require('fs').readFileSync(require('path').normalize(args[1]), "utf8");
    return exports.parser.parse(source);
};
if (typeof module !== 'undefined' && require.main === module) {
  exports.main(process.argv.slice(1));
}
}
...
```

#### <a name="apidoc.element.jsonpath.parser.parse"></a>[function <span class="apidocSignatureSpan">jsonpath.parser.</span>parse ()](#apidoc.element.jsonpath.parser.parse)
- description and source-code
```javascript
parse = function () { return parser.parse.apply(parser, arguments); }
```
- example usage
```shell
...
//   { path: ['$', 'store', 'book', 0, 'author'], value: 'NIGEL REES' },
//   { path: ['$', 'store', 'book', 1, 'author'], value: 'EVELYN WAUGH' },
//   { path: ['$', 'store', 'book', 2, 'author'], value: 'HERMAN MELVILLE' },
//   { path: ['$', 'store', 'book', 3, 'author'], value: 'J. R. R. TOLKIEN' }
// ]
'''

#### jp.parse(pathExpression)

Parse the provided JSONPath expression into path components and their associated operations.

'''javascript
var path = jp.parse('$..author');
// [
//   { expression: { type: 'root', value: '$' } },
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

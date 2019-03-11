# JS Modules

JavaScript files can be imported directly in your Clio code. For JavaScript files you need to use `exports` or `module.exports` variables:

{% code-tabs %}
{% code-tabs-item title="my\_module.js" %}
```text
module.exports.hello = function(name) {
    console.log(`Hello ${name}`);
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

and to import it in Clio:

```text
import hello from my_module.js
```

When importing JavaScript files you must include `.js` in the file name. Same as Clio modules, these imports are relative and recognize the same path formats as the Clio file imports.

Currently, Clio doesn't support direct Node.js module imports. For now, to import a Node.js module either import the main JavaScript file of the package, or `require` them in a JavaScript file and import that JavaScript file. As an example:

{% code-tabs %}
{% code-tabs-item title="rethinkdb.js" %}
```text
module.exports.rethinkdb = require('rethinkdb');
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Then in a Clio file:

```text
import rethinkdb from rethinkdb
```




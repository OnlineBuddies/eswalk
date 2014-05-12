eswalk
======

Walks an Esprima parse tree

Example:

    var eswalk = require('eswalk');

    eswalk(tree, function(node, parent) {
        if (node.type == 'ExpressionStatement' &&
            node.expression.type == 'CallExpression' &&
            node.expression.callee.name == 'define') {
            doSomethingWith(node.expression);
        }
    });

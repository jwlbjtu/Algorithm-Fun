## Walk Tree Structure
> 1. Define a function that visits every node of the tree structure
> 2. Define a function to find matching nodes from a tree structure

### JavaScript
```javascript
var walk_the_tree = function walk(node, func) {
    func(node);
    node = node.firstChild;
    while(node){
        walk(node, func);
        node = node.nextSibling;
    }
};

var getNodeByAttribute = function (att, value) {
    var result = [];

    walk_the_tree(node, function(node) {
        var actual = node.nodeType === 1 && node.getAttribute(att);
        if (typeof actual === 'string' &&
            (actual === value || typeof value !== 'string')) {
                result.push(node);
            }
    });

    return result;
};

```
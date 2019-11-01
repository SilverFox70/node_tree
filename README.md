## Tree

This is a basic implementation of a tree in node.js

## Classes

<dl>
<dt><a href="#Node">Node</a></dt>
<dd><p>Class representing a node in the tree</p>
</dd>
<dt><a href="#Tree">Tree</a></dt>
<dd><p>Class representing a tree.</p>
</dd>
</dl>

<a name="Node"></a>

## Node
Class representing a node in the tree

**Kind**: global class
<a name="new_Node_new"></a>

### new Node(data)
Creates a new Node for use in the tree.


| Param | Type | Description |
| --- | --- | --- |
| data | <code>Object</code> | The data to be stored in the node |

<a name="Tree"></a>

## Tree
Class representing a tree.

**Kind**: global class

* [Tree](#Tree)
    * [new Tree(data, meta)](#new_Tree_new)
    * [.breadthFirstTraverse(callback)](#Tree+breadthFirstTraverse)
    * [.depthFirstTraverse(callback)](#Tree+depthFirstTraverse)
    * [.contains(callback, traversal)](#Tree+contains)
    * [.addNode(data, parentNode, traversal)](#Tree+addNode) ⇒ <code>string</code>
    * [.removeNode(node, traversal)](#Tree+removeNode) ⇒ <code>string</code>

<a name="new_Tree_new"></a>

### new Tree(data, meta)
Creates a new instance of a tree where 'data' become the data the root node.


| Param | Type | Description |
| --- | --- | --- |
| data | <code>Object</code> | Data object for the root node of the tree. |
| meta | <code>Object</code> | Any meta data you would like to add for the tree. |

<a name="Tree+breadthFirstTraverse"></a>

### tree.breadthFirstTraverse(callback)
Perform a breadth firts traversal of the tree.

**Kind**: instance method of <code>[Tree](#Tree)</code>

| Param | Type | Description |
| --- | --- | --- |
| callback | <code>function</code> | The callback function takes two parameters, a Node and an index. Node is the tree node and index is the index of the tree level where 0 is root. |

<a name="Tree+depthFirstTraverse"></a>

### tree.depthFirstTraverse(callback)
Perform a depth first traversal for the tree.

**Kind**: instance method of <code>[Tree](#Tree)</code>

| Param | Type | Description |
| --- | --- | --- |
| callback | <code>function</code> | The callback function takes two parameters, a Node and an index. Node is the tree node and index is the index of the tree level where 0 is root. |

<a name="Tree+contains"></a>

### tree.contains(callback, traversal)
First iteration of a matching function.

**Kind**: instance method of <code>[Tree](#Tree)</code>

| Param | Type | Description |
| --- | --- | --- |
| callback | <code>function</code> | Used to check against whatever props of the node you desire. |
| traversal | <code>function</code> | Method used to traverse the tree, defaults to depth first |

<a name="Tree+addNode"></a>

### tree.addNode(data, parentNode, traversal) ⇒ <code>string</code>
Adds a node to the tree. The node's data will be the
data arg passed in, and the parent will be the
parentNode.

**Kind**: instance method of <code>[Tree](#Tree)</code>
**Returns**: <code>string</code> - Return the ID of the new child node.

| Param | Type | Description |
| --- | --- | --- |
| data | <code>Object</code> | The data to stored in the node. |
| parentNode | <code>Object</code> \| <code>string</code> | The parent node or its ID. |
| traversal | <code>function</code> | The method to use to traverse the tree, default is depth first. |

<a name="Tree+removeNode"></a>

### tree.removeNode(node, traversal) ⇒ <code>string</code>
Removes a node given the node or its ID.

**Kind**: instance method of <code>[Tree](#Tree)</code>
**Returns**: <code>string</code> - Returns the id of the parent node of the removed item.

| Param | Type | Description |
| --- | --- | --- |
| node | <code>Object</code> \| <code>string</code> | The node or the id of the node to be removed. |
| traversal | <code>function</code> | The function for traversing the tree, default to depth first. |
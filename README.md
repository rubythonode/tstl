# TypeScript-STL
[![NPM](https://nodei.co/npm/tstl.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/tstl)
  - GitHub Repository: https://github.com/samchon/tstl
  - Guide Documents: https://github.com/samchon/tstl/wiki


## Introduction
STL (Standard Template Library) *Containers* and *Algorithms* for the **TypeScript**.

**T**ypeScript-**STL** is an open-source project providing **containers** and **algorithms** migrated from *C++ STL* to *TypeScript*. You can enjoy the STL's own specific *coantainers* and *algorithms* in the JavaScript. If TypeScript, you also can take advantage of type restrictions and generic programming with the TypeScript.

Below components are list of provided objects in the **T**ypeScript-**STL**. If you want to know more about the **TypeScript-STL**, then please read the [**Guide Documents**](https://github.com/samchon/tstl/wiki).

### Containers
  - **Linear Containers**
    - [Vector `vector`](http://samchon.github.io/tstl/api/classes/std.vector.html)
    - [List `list`](http://samchon.github.io/tstl/api/classes/std.list.html)
    - [Deque `deque`](http://samchon.github.io/tstl/api/classes/std.deque.html)
  - **Associative Containers**
    - *Tree-structured Containers*
      - [TreeSet `set`](http://samchon.github.io/tstl/api/classes/std.treeset.html)
      - [TreeMultiSet `multiset`](http://samchon.github.io/tstl/api/classes/std.treemultiset.html)
      - [TreeMap `map`](http://samchon.github.io/tstl/api/classes/std.treemap.html)
      - [TreeMultiMap `multimap`](http://samchon.github.io/tstl/api/classes/std.treemultimap.html)
    - *Hash-buckets based Container*
      - [HashSet `unordered_set`](http://samchon.github.io/tstl/api/classes/std.hashset.html)
      - [HashMultiSet `unordered_multiset`](http://samchon.github.io/tstl/api/classes/std.hashmultiset.html)
      - [HashMap `unordered_map`](http://samchon.github.io/tstl/api/classes/std.hashmap.html)
      - [HashMultiMap `unordered_multimap`](http://samchon.github.io/tstl/api/classes/std.hashmultimap.html)
  - **Adaptor Containers**
    - [Queue `queue`](http://samchon.github.io/tstl/api/classes/std.queue.html)
    - [Stack `stack`](http://samchon.github.io/tstl/api/classes/std.stack.html)
    - [PriorityQueue `priority_queue`](http://samchon.github.io/tstl/api/classes/std.priorityqueue.html)

### Global Functions
  - [`<algorithm>`](http://www.cplusplus.com/reference/algorithm/)
  - [`<exception>`](http://www.cplusplus.com/reference/exception/)
  - [`<functional>`](http://www.cplusplus.com/reference/functional/)
    - [IComparable](http://samchon.github.io/tstl/api/interfaces/std.icomparable.html)
  - [`<utility>`](http://www.cplusplus.com/reference/utility/)
    - [Pair `pair`](http://samchon.github.io/tstl/api/classes/std.pair.html)



## Installation
### NPM Module
Installing **TSTL** in *NodeJS* is very easy. Just install with the `npm`

```bash
# Install TSTL from the NPM module
npm install --save tstl

# If you need only definition, then fetch from the @types
npm install --save-dev @types/tstl
```

### Usage (TypeScript)
``` typescript
/// <reference types="tstl" />
import std = require("tstl");

let map: std.TreeMap<number, string> = new std.TreeMap<number, string>();

// INSERT ITEMS
map.insert(std.make_pair(1, "First"));
map.insert([4, "Fourth"]); // via Tuple, C++11 Feature
map.insert_or_assign(5, "Fifth"); // C++17 Feature
map.set(9, "Nineth");

// ITERATION
for (let it = map.begin(); !it.equals(map.end()); it = it.next())
	console.log(it.first, it.second); // (key => number, value => string)

// LOWER_BOUND
let x = map.lower_bound(3);
console.log("lower bound of 3 is: " + x.first + ", " + x.second);
```

### In Browser
**TypeScript-STL** follows the `CommonJS` module. 

Use [browserify](https://www.npmjs.com/package/browserify) or just include the **TypeSript-STL**'s JS file with the `<script>` tag.

```html
<script src="http://samchon.github.io/dist/tstl.min.js"></script>
```



## References
  - **Repositories**
    - [GitHub Repository](https://github.com/samchon/tstl)
    - [NPM Repository](https://www.npmjs.com/package/tstl)
  - **Documents**
    - [**Guide Documents**](https://github.com/samchon/tstl/wiki)
    - [API Documents](http://samchon.github.io/samchon/tstl)
    - [Class Diagram](http://samchon.github.io/tstl/design/class_diagram.pdf)
  - **Related Projects**
    - [Samchon-Framework](https://github.com/samchon/framework)
    - [3D-Bin-Packing](https://github.com/betterwaysystems/packer)
# RoseTree
Rosetree is the C++ implementation for the data structure of the same name. Rosetrees are generic trees with unbounded numbers of branches at each node

Link to references about Rosetree:
* https://en.wikipedia.org/wiki/Rose_Tree
* https://cs.stackexchange.com/questions/56081/what-are-the-applications-of-rose-trees

RoseTree aims to be a header only library, compatible with the STL algorithms
like std::transform, std::find etc.

The data structure is unsorted, unbalanced tree. Users are
allowed to insert data from top to bottom and left to right

## Basic API documentation
### Tree construction

```c++
auto path_tree = Tree(new TreeNode<std::string>("/"));

auto boot = path_tree.insert_below(path_tree.begin(), std::string("boot/"));
auto bin = path_tree.append_child(path_tree.begin(), std::string("bin/"));
auto var = path_tree.append_child(path_tree.begin(), std::string("var/"));
auto usr = path_tree.append_child(path_tree.begin(), std::string("usr/"));
```

### Tree insertion operations

### Tree deletion operations

### Tree iteration
Currently supported iterators:
* Breadth-First Iterator
* PreOrder Depth-First Iterator
* PostOrder Depth-First Iterator

The default iterator on constructing a tree will be PreOrder iterator. Proxy
classes are available to convert the default iterator to other types

## Roadmap
- [x] Iterators - PreOrder, PostOrder, LevelOrder
- [x] Insertion APIs - Value Semantics
- [x] Insertion APIs - Move Semantics
- [x] Insertion APIs - Emplacing / In place construction of nodes
- [x] Deletion - Erase node
- [x] Deletion - Subtree eviction by cutting
- [x] Deletion - Clear container
- [ ] Iterators - InOrder, LeafOrder
- [x] Automatic memory cleanup on destruction
- [ ] Tree copy - Deep
- [ ] Tree move
- [ ] Tree head manipulation
- [ ] Iterators - const versions



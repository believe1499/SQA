#Basic Concepts of DDG(Data Dependency Graph)
<b>The Homework for Week 4 By Fang Xiaobin (方晓斌 13126067) From Group C</b>
<hr>
The test cases are derived from data dependency analysis (DDA), with a focus on D-U relations, and the related model we call data dependency graph (DDG).

In DDGs, each node represents the definition of a data item, such as a variable, a constant, and a compound data structure. The links in DDGs represent the D-U relation, or “is used by”. That is, if we have a link from A to B, we interpret it as that the data defined in A is used to define the data in B.This analysis of chains of D-U relations used in defining later data items can be carried out to identify the definitions of those earlier items, until we resolve all the definitions.

We can view a DDG as a logical graph where computational results are expressed in terms of input variables and constants through the possible use of some intermediate data items as nodes and related D-U relations as links.

We can consider a DDG as consisting of input nodes, output nodes, intermediate nodes, data selector nodes, and associated links and properties. Again, the focus is on the output or results, and their resolution through DDGs in terms of input variables and constants. Because of this procedure for data resolution through backward chaining using D-U relations, the DDGs typically show the following characteristics:

* There is usually one output data itern or variable, or at most a few of them.
* There are typically more input variables and constants.
* Multiple inlinks are common.
* Since the DDG is typically shown as flowing from top to bottom, we have the “fan” shaped DDGs as the most common type. This shape is also often described as tree-shaped (like a real tree on the ground, not the upside-down ones in computing literature), or shaped like a river with its tributaries.

# Software Analysis

There are 3 kinds of things in software.

* Being - Data
* Doing - Program, to take input data and generate the output data. It also refers a workflow that connects smaller program and data.
* Timing - Event, both as result of program, and as trigger to program.

It is important to figure out the instance relationship among them in your software. The following diagram are the way to design your software with quality and ease.

## Static

Class hierarchy, standard way

Inter-Class Composition and Interaction - Object Graph

Decoupling

### Data derivation (cause-effect) graph.

Example:

* Image (Generated or modified ) -> Data -> URL (in local file)

## Dynamic (debugging the program and set breakpoints)



### Inter-function call trace graph

Goals:

* breaking down the responsibilities of func's, until meeting *nearly* single responsibility.
* minimizing the amount of data passing through functions.  

Code Improvement: strengthen types' and members' access scope. the smaller, the bigger and safer.

### Operation - Data relationship.

Operations can be categorized into 2 groups, data mutating (also called write, modify) and data non-mutating (also called read, query).

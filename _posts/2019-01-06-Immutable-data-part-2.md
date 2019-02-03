---
layout: post
title: Immutable data part 2
---

The question of mutability of data items is tied up with the question of aggregation - what constitutes a single "item" in a data set? For example, suppose you were interested in modeling the performance of machines over time. You could model each machine as a separate item, but what should happen if the machine is repaired and some important parts are replaced? Should it be considered a new machine? Or should the machines be modeled as a collection of parts?


One approach to mutability is to simply declare that data items present at different points in time are to be treated as distinct. So, instead of modeling the items in a data set as <i>d<sub>1</sub>, d<sub>2</sub>, ..., d<sub>m</sub></i> where an item may change at some time, the data set is modeled as {<i>d<sub>i,t</sub></i>}, where <i>i</i> indicates the identity of the item, and <i>t</i> indicates a point in time. It seems obvious that item identities should be tracked; for instance, one might want to only consider the most recent version of each item, or ensure that different versions of the same item are kept together in a train/test split.

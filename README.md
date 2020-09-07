# BiMap
An ordered bidirectional map data structure providing slicing the set of associations on both key and values. 

# Requirement 
A bunch of algorithmic questions need capability to access a set of associations via filter operations on keys as well as values. 
e.g. 
- Find the next nearest largest value (>A[n]) post the nth element of an array when travering from left to right.
- and a bunch of other similar requirements.

The BiMap should provide functionalities similar to a TreeMap (head, tail, floor, ceil, submap) for both Keys and Values. 
Each filter operation should return a view on which subsequent filtering can be done. 

Complexity Requirements for a BiMap of N associations (key, Value)
Creation of the BiMap - O(NLogN)
Insert, Delete operations - O(LogN)
head, tail operations - O(1)
floor, ceil operations - O(LogN)

Space Complexity - O(N) => higher constant associated with this upper bound. 

# Design of BiMap

TreeMap<Key, Map.Entry> --->. LinkedHashMap<Key,Value> <----- TreeMap<Value, Map.Entry>


The above design _should_ provide all treeMap functionalities on Keys and Values. Also it should provide a way to jump filter pivots from Keys to Values using the Map.Entry

TreeMap on Key and Value will provide _natural_ ordering on Keys and Values.
LinkedHashMap will provide insertion ordering between the keys.

WIP.

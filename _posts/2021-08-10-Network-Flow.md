---
title: "Network Flow Problems"
categories:
  - Learning
---

General Setup of the Problem:

Imagine a complex network of ONE WAY roads connecting cities. This can be thought of as a graph. Each city(node) may have zero or more roads(edges) entering and leaving it. 
Each road has a CAPACITY(maximum cars that can move on the road) and FLOW(number of cars currently on a road). Every car that enters a city has to leave it.
Problem is to maximize the FLOW(number of cars) from a source city to a destination city. This has to be done while keeping flow on each road as per it's capacity.

What makes the problem hard?
The road flow is a local contraint. Decreasing the flow for a local edge might increase the overall flow from source to sink and vice versa. In  a graph edges incease as N^2 with linear increase in vertices. Optimizing a global objective with local constraints rising at N^2 rate is the problem.


(Note: Cycles with two nodes are coverted to 3 node cycles by introducing an auxiliary node)
Algorithm to solve problem:
We define a residual network to find the solution. The residual network represents the graph with edges as possible increases and decreases in flow.
So the weight of the edge in direction as original graph is (Capacity - flow) as this how much the flow can be increased by. Weight of the edge in the opposite direction is equal to the flow as we can decrease the flow by this amount in orignal graph to make it zero.

The algorithm states that we can find a path from source to target(augmented path) in the residual network, then the network flow is sub-optimal. 
The flow of the augmented path is found and tweaked in the original graph.
The residual graph is calculated again and process continues until no augmented path exists in residual network.


 Sidenotes:

 Graph Cut - partition vertices into two disjointed sets. 
 Cut Set - Set of edges of graph that were cut

 Flow Network S-t cut - A cut in which Source and Target are in different sets

 Max Flow Min Cut Theorem - Value of any Flow in bounded by capacity of any cut in a network.
    Note - Flow can be negative(Convention to account for opposite flow) but capacity is always positive.

Lemma - Flow of a network is the flow across any cut(s-t). 
        Since flow across cut is bounded by capacity of cut, max flow min cut follows from this lemma


Residual Network - It is the orginal graph without the edges flowing at full capacity. Naturally it is defined for a particluar flow.
                  The edges operating at suboptimal capcity have a corresponding negative egdge(edge in reverse direction) with the   
                


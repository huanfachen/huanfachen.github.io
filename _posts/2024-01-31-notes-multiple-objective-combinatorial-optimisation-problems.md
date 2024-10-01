---
title: 'Notes on multiple objective combinatorial optimisation problems'
date: 2024-01-31
permalink: /posts/2024/01/Notes_multiple_objective_optimisation/
tags:
  - Optimisation
  - MultipleObjective
  - MOO
---

Updates 2024/01/31

This post records some notes on multi-objective combinatorial optimization (MOCO) problems.

## Categorisation of strategies

Ehrgott and Gandibleux [7] categorised solution methods for addressing multi-objective optimization problems into three groups, based on the information provided by decision-makers. These groups are as follows:

- Priori mode: In this strategy, decision-makers express their preferences at the beginning of the process. An example of this approach is **goal programming**, where decision-makers specify their objectives upfront.
- Posteriori mode: The preferences of decision-makers are analyzed after obtaining all the non-dominated points. This mode focuses on evaluating and comparing different solutions based on the decision-makers’ preferences. Some algorithms of this approach aim to obtain the entire non-dominated frontier. These algorithms involve reformulating the multiple-objective problem as a collection of single-objective models. Two effective approaches are the two-phase method and $\epsilon$-constraint method.
- Interactive mode: This strategy involves active involvement and collaboration between decision-makers and the decision-making process. Decision-makers play a significant role, providing feedback and refining their preferences during the computation steps.

## Goal programming

Here, for each of the objectives a target value (goal) is specified by the decision maker. The overall aim is to minimize the deviation from the specified goals. This approach is sometimes considered a different field from multiobjective optimization. 

A good example of goal programming can be found [here](https://www3.eng.cam.ac.uk/~dr241/3E4/Lectures/3E4%20Lecture%206.pdf).

Other references on GP

- Ignizio JP (1976) Goal programming and extensions. Lexington Books,Lexington, KY

- Lee SM (1972) Goal Programming for decision analysis. Auerbach,Philadelphia,PA

## Efficient solution and supported solution

## Lexicographic optimization

## Max-ordering problem

As far as the other definitions of optimality in (MOCO) are concerned,we note that the max-ordering problem with sum objectives is INP -hard in general (see [22]), but can be reduced to a single objective problem in the case of **bottleneck objectives**. 

For lexicographic optimization it is known that a lexicographically optimal solution is always efficient,and even a supported efficient solution
---
title: "Cache Simulator"
created: March 2020
collections: portfolio
order: 1030
---
Cache Simulator is a project that aims to simulate how cache on processors behave. The purporse of the cache is to provide quick memory storage for the processor because accessing RAM and hard drive is slow. Processors generally have high frequencies, so it might take hundreds of cycle to get data from RAM and thousands of cycles to get data from the hard drive. On the other hand, it would take a few cycles to retrieve data from cache.

A cache has a number of properties: 
- number of sets
- number of blocks
- write allocation or no write allocation
- write back or write through
- eviction style (least recently used or first-in-first-out)

These properties affect how a cache behaves and its performance. The best cache configuration minimizes the number of cache misses (when memory is not in the cache and needs to be retrieved before being used) and total cycles for loading and accessing memory.

The Cache Simulator program would be given a memory trace as input and it would determine the total loads, total stores, load hits, load misses, store hits, store misses, and total cycles.

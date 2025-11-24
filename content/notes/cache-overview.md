+++
title = 'Cache Overview'
date = 2025-08-24
toc = true
tocBorder = true
+++
## What is Cache?
Simply put: **a cache is a small, fast memory that stores frequently used or nearby data to improve performance.**

---

## Performance
To understand why caching improves performance, we need to consider **buffering**, the **principle of locality**, and **prefetching**.  

The goal is to **maximize cache hits** (when requested data is found in the cache) and **minimize cache misses** (when it isn’t).  

### Buffering
A cache temporarily stores data — a form of buffering — so the system can avoid fetching it again from slower memory.  

### Principle of Locality
Applications typically follow the *principle of locality* when accessing data:  
- **Temporal Locality:** If data is accessed, it is likely to be accessed again soon.  
- **Spatial Locality:** If data is accessed, data located nearby is likely to be accessed as well.  

### Prefetching
The system may also predict which data will be needed soon and proactively load it into the cache.  

---

## Management
Because cache memory is small, it must be managed carefully. This is done through **eviction (replacement) policies**, which decide which data to keep and which to discard when space is needed.  

### Common Eviction Policies
- **LRU (Least Recently Used):** Evict the data that hasn’t been accessed for the longest time.  
- **LFU (Least Frequently Used):** Evict the data used least often.  
- **Random:** Evict a randomly chosen cache entry.  

---

## References
- [Wikipedia: Cache (computing)](https://en.wikipedia.org/wiki/Cache_(computing)#Operation)

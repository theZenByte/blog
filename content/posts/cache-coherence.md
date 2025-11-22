+++
title = 'Cache Coherence'
date = 2025-08-25
toc = true
tocBorder = true
+++
## What is Cache Coherence?
Simply put: **cache coherence ensures that when data is written in one cache, all other caches see the updated value.** 

---

## A Cache Coherent System 
For a system to be truly coherent, two key properties must hold: 

### Write Propagation 
When one processor writes to a piece of data, that change must eventually become visible to all other processors when they read it. 

### Transaction Serialization 
All processors must agree on the order of reads and writes. This guarantees that no processor reads a stale value — the latest written value is always the one read. 

---

## Management 
Cache coherence is enforced using core **mechanisms**, which are applied through various **protocols.**

### Mechanisms 
These mechanisms are different methods of keeping track of changes (writes) made to shared data in caches. 
- **Snooping:** Caches monitor (or "snoop") bus transactions, such as reads and writes to memory. 
- **Directory-based:** Caches use a common directory that tracks which caches hold copies of data. 

### Protocols 
Protocols are implementations of these mechanisms. 
- **MSI (Modified, Shared, Invalid)** 
- **MESI (Modified, Exclusive, Shared, Invalid)** 
- **MOESI, MESIF, etc.** (more advanced variants) 

---

## References  
- [Wikipedia: Cache Coherence](https://en.wikipedia.org/wiki/Cache_Coherence) 


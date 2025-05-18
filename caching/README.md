# Python Caching Strategies

## Overview

This repository contains my implementation of several classic caching strategies in Python. The goal of the project is to demonstrate a deep understanding of memory optimization techniques and cache replacement algorithms by simulating how data might be managed in real-world systems.

Each strategy is implemented as a Python class, with consistent behavior for setting and retrieving cache entries, while managing data according to the defined eviction policy.

## Implemented Caching Strategies

### 1. **BasicCache**
A simple dictionary-based cache without any eviction logic. Ideal for understanding the fundamentals.

### 2. **FIFOCache** (First-In, First-Out)
Evicts the oldest added item when the cache reaches its limit.

### 3. **LIFOCache** (Last-In, First-Out)
Evicts the most recently added item when the cache reaches its limit.

### 4. **LRUCache** (Least Recently Used)
Tracks usage order and evicts the item that hasn't been used in the longest time.

### 5. **MRUCache** (Most Recently Used)
Evicts the most recently accessed item — useful in some database or session caching scenarios.

### 6. **LFUCache** (Least Frequently Used)
Evicts the item used the least number of times. If there’s a tie, the least recently used among them is removed.

## Folder Structure

```

.
├── base\_caching.py        # Base class defining the structure of all caches
├── 0-basic\_cache.py       # BasicCache implementation
├── 1-fifo\_cache.py        # FIFO strategy
├── 2-lifo\_cache.py        # LIFO strategy
├── 3-lru\_cache.py         # LRU strategy
├── 4-mru\_cache.py         # MRU strategy
├── 100-lfu\_cache.py       # LFU strategy
├── main\_\*.py              # Sample test scripts
└── README.md              # Project documentation

````

## How to Use

You can run any of the `main_*.py` files to test a specific cache class:

```bash
python3 main_1.py
````

You may also import and use any cache class in your Python project like this:

```python
from lru_cache import LRUCache

cache = LRUCache()
cache.put("key1", "value1")
print(cache.get("key1"))
```

## Requirements

* Python 3.8 or higher
* No external libraries required

## Author

- **Daniel Iryivuze**
- Software Developer | Python Enthusiast
- 📍 Kigali, Rwanda
---

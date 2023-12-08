# Priority-expiry-cache 

### Overview

Boost your cache efficiency in case you have a priority of the pages and an expiration time of the page.

The eviction policy follows these steps in case of a tie goes to the following:
  - oldest expired 
  - lowest priority
  - LRU

Set Operation: O(1) time and space

Get Operation: O(1) time and space

Evict Operation: O(1) time and space

Wrapper in Python for the Rust cargo [cargo](https://crates.io/crates/priority-expiry-cache)

Published on PyPI https://pypi.org/project/priority-expiry-cache/

### install 

```pip install priority-expiry-cache```

### quick start

```python
from priority_expiry_cache import PECache

new_cache = PECache()
# add an item to the cache key,value,priority,expiration
new_cache.set(key="key", value="value",priority=2,expiry=10)
# get an item from the cache
new_cache.get(key="test")
# evict remove the item following the policy setting the barrier
new_cache.evict(barrier=0)
```



## Credits
- [Giacomo Sorbi](https://www.linkedin.com/in/giacomosorbi/) for proofreading
- [Maturin](https://pypi.org/project/maturin/) for the wrapper scaffolding

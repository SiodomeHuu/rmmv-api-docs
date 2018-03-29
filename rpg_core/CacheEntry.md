CacheEntry
===

# Father:

# Functions:
* Constructor(cache,key,item)
* [touch()](#touch)
* setTimeToLive(ticks,seconds)
* allocate()
* [free(byTTL)](#free)
* isStillAlive()

# Members:
* cache (Resource Manager)
* key
* item
* cached
* touchTicks
* touchSeconds
* ttlTicks
* ttlSeconds
* freedByTTL

# Details:

<p id="free"></p>

* free(byTTL):
    * if this is not cached, pass
    * else, delete this
    * byTTL means whether this is freed by TTL or not

<p id="touch"></p>

* touch():
    * if cached, set ttl to max
    * if freed by ttl, put in cache again
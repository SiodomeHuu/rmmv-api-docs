CacheMap
===

# Notes: Cache for images, audio, or any other kind of resource

# Notes2: No need to look deep into

# Father:

# Functions:
* Constructor(manager)
* clear()
* checkTTL()
* setItem(key,item)
* getItem(key)
* update(ticks, delta) delta->seconds

# Members:
* manager
* _inner
* _lastRemovedEntries
* updateTicks
* lastCheckTTL
* delayCheckTTL
* updateSeconds

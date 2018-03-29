ImageCache
===

# Father:

# Functions:
* Constructor(*arg)
* isReady()
* getErrorBitmap()
* [get(key)](#get)
* [releaseReservation(reservationId)](#releaseReservation)
* [add(key, value)](#add)
* [initialize()](#initialize)
* [reserve(key, value, reservationId)](#reserve)
* [_truncateCache()](#_truncateCache)
* _mustBeHeld(item)

# Members:
* limit = 10000000
* _items


#Details:

<p id="initialize"></p>

* initialize()
    * set _items={}

<p id="add"></p>

* add(key,value)
    * _items[key]={ bitmap:value, touch:Date.now(), key:key}

<p id="get"></p>

* get(key)
    * get and **Touch**

<p id="reserve"></p>

* reserve(key,value,reservationId)
    * new Property in _items: reservationId

<p id="releaseReservation"></p>

* releaseReservation(reservationId)
    * delete by id

<p id="_truncateCache"></p>

* _truncateCache()
    * delete those who not used long **AND** not a must to be held
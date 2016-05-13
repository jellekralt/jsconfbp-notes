# Building an offline page for theguardian.com
*Oliver Joseph Ash* [@OliverJAsh]()

---
## Service workers
* listen to push events, useful for pushing notifications
* intercept and handle network requests
* Future
  * geofencing
  * alarms
* Progressive enhancement

```
navigator.serviceWorker
```

### Install event
* install event
* cache the assets needed later
* Version the cache

### Fetch events
* Intercept network requests to:
  * fetch from the network
  * read from the cache

### Mutable vs Immutable

* Mutable (HTML) and Immutable (CSS) requests
  * Mutable: Network first, cache second
  * Immutable: Cache first, network second

### Problems & Caveats
* Browser bugs in both Chrome and FF
* Interleaving of versions in CDN cache
  * Solution: Cache manifest

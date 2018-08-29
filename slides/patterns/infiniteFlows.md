## Creating infinite publisher

Can be very useful for composing flows where number of items is unknown.  
Reminder: infinite publisher doesn't mean an infinite number of emitted items.

```
Flux.range(0, MAX_VALUE)
    .map(i -> somethingUseful())
```

When time matters:
```
Flux.interval(duration)
    .map(i -> somethingUseful())
```
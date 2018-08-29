## Creating infinite publisher

Repeat the same sequence indefinitely :
```
myFlux.repeat()
```

at fixed intervals :
```
Flux.interval(duration).flatMap(tick -> myFlux)
```
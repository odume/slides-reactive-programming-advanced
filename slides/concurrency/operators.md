## Concurrency operators

switch the rest of the flux on another thread
```
.publishOn(scheduler)
```

<br>

make the subscription and requests happen on another thread
```
.subscribeOn(scheduler)
```
  

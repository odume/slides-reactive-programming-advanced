## Alternate scenario - fallback

Try a primary scenario and switch to another one if it didn't succeed, without errors.

```
Flux.concat(primary, fallback).next();
```

* ```primary``` is empty when it doesn't work (tip: think about ```filter()```)
* ```next()``` only takes the first emitted item (by primary or fallback) and returns a ```Mono```
* ```concat()``` will not subscribe to ```fallback``` if ```primary``` makes the job 
* ```next()``` can be replaced by ```takeWhile()``` or ```takeUntil()``` for multiple results (```Flux```)

Reactor provides a simple operator

```
primary.switchIfEmpty(fallback);
```
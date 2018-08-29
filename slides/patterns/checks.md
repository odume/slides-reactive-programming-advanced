## Checks

Characteristics of checks:
* Can access the object
* Does not change the object
* Can throw errors when something is wrong

Best option is to use a simple ```doOnNext(consumer)``` 

* consumer can throw (runtime) exceptions
* consumer cannot change the object
## Try-Catch : error recovery

Some operators listen only to error events:

* ```onErrorReturn(T value)``` : swallow error and return a value instead, then complete. i.e. Catch and return a static default value
* ```onErrorResume(Publisher<T> publisher)``` : swallow error and resume with another provided publisher. i.e. Catch and execute an alternative path with a fallback method
* ```onErrorMap(Function mapper)``` : map the error to another one. i.e. Catch, wrap the exception and rethrow
* ```onError(consumer)``` : Usually used for logging
* ```doFinally(consumer)``` : Add behavior **after** the flux terminates
* ```retry()``` : Swallow error and resubscribes
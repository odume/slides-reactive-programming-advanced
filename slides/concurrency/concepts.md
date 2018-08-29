## Concepts

By default, Reactor (and all reactive extensions) are agnostic on concurrency. In other words, everything happens on the same thread:
* The construction of the Publisher
* The subscription
* The emission (request) of items
* The treatment of these items by operators

It is possible to change that behavior by declaring which parts should be executed on a different thread.
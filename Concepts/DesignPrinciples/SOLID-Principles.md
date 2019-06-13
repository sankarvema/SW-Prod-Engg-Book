# SOLID Design Principles

## Single Responsibility

A class should have one and only one reason to change, meaning that a class should only have one job.

## Open Closed

Objects or entities should be open for extension, but closed for modification.

## Liskov substitution

Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T.

In simple terms, a subclass should override the parent class methods in a way that does not break functionality from a client’s point of view.

## Interface Segregation

A client should never be forced to implement an interface that it doesn’t use or clients shouldn’t be forced to depend on methods they do not use

## Dependency inversion

Entities must depend on abstractions not on concretions. It states that the high level module must not depend on the low level module, but they should depend on abstractions.

## References

https://medium.com/@cramirez92/s-o-l-i-d-the-first-5-priciples-of-object-oriented-design-with-javascript-790f6ac9b9fa

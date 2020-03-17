# c++ features

## c++ 11

### LValue RValue
An lvalue (locator value) represents an object that occupies some identifiable location in memory (i.e. has an address).
rvalues are defined by exclusion that does not represent an object occupying some identifiable location in memory.

### Forwarding references
This enables perfect forwarding: the ability to pass arguments while maintaining their value category (e.g. lvalues stay as lvalues, temporaries are forwarded as rvalues).

Forwarding references allow a reference to bind to either an lvalue or rvalue depending on the type. Forwarding references follow the rules of reference collapsing:

- T& & becomes T&
- T& && becomes T&
- T&& & becomes T&
- T&& && becomes T&&

auto type deduction with lvalues and rvalues:
```
int x = 0; // `x` is an lvalue of type `int`
auto&& al = x; // `al` is an lvalue of type `int&` -- binds to the lvalue, `x`
auto&& ar = 0; // `ar` is an lvalue of type `int&&` -- binds to the rvalue temporary, `0`
```

ex) https://github.com/AnthonyCalandra/modern-cpp-features#forwarding-references

## c++ 14

## c++ 17

## c++ 20

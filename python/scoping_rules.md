When trying to mutate a var with a primitive value in an enclosing scope,
Python will need to make a copy to shadow the original.

```python

def foo():
    x = 0
    def _(): x += 1
    return _
```

This does not work because x holds a primitive value. Python requires a copy to
mutate.

```python

def foo():
    x = [0]
    def _(): x[0] += 1
    return _
```

This works fine because _ accesses x from the enclosing scope via reference.

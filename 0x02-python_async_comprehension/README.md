0x02-python_async_comprehension

### Asynchronous Generators

An asynchronous generator is defined using `async def` and `yield`. It allows you to write functions that can await asynchronously within their body. Use the `yield` keyword to produce values.

Example:

```python
async def async_gen():
    for i in range(10):
        yield i
```

### Async Comprehensions

Async comprehensions are used to create lists, sets, and dictionaries asynchronously. They can await asynchronous generators within comprehensions.

Example:

```python
result = [i async for i in async_gen()]
```

### Type-annotate Generators

To type-annotate generators, use `Generator` from `typing` for synchronous generators and `AsyncGenerator` for asynchronous ones.

Example:

```python
from typing import AsyncGenerator

async def async_gen() -> AsyncGenerator[int, None]:
    for i in range(10):
        yield i
```

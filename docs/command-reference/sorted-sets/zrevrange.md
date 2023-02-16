---
description: Return a range of members in a sorted set, by index, with scores
  ordered from high to low
---

# ZREVRANGE

## Syntax

    ZREVRANGE key start stop [WITHSCORES]

**Time complexity:** O(log(N)+M) with N being the number of elements in the sorted set and M the number of elements returned.

Returns the specified range of elements in the sorted set stored at `key`.
The elements are considered to be ordered from the highest to the lowest score.
Descending lexicographical order is used for elements with equal score.

Apart from the reversed ordering, `ZREVRANGE` is similar to `ZRANGE`.

## Return

[Array reply](https://redis.io/docs/reference/protocol-spec#resp-arrays): list of elements in the specified range (optionally with
their scores).

## Examples

```cli
ZADD myzset 1 "one"
ZADD myzset 2 "two"
ZADD myzset 3 "three"
ZREVRANGE myzset 0 -1
ZREVRANGE myzset 2 3
ZREVRANGE myzset -2 -1
```

## Exercise I

#### a) O(n)

While this algorithm would not linearly run _every_ element between 0 and n (because it jumps by `n^2` each time), the log time reduces to `O(n)`, linear run time complexity.


#### b) O(n) * O(n) * O(n) * O(1) = O(n^3)

The outer loop will run `O(n)`, hitting every element between 0 and n.
The j nested loop will hit fewer elements (between 1 and n) but still runs lineary `(O(n))`.
The k nested loop will hit even fewer elements (between 2 and n) but still runs linearly `(O(n))`.
The l nested loops run constant time (between k+1 and k+10, or 10 loops each time), so evaluates to `O(1)`.  


#### c) O(n)

This recursive algorithm calls upon itself, which means it has to resolve itself down to the base case before returning an open call (creating a large call stack); but it only calls upon itself once each time, so the run time is still `O(n)`.


<br>

## Exercise II

To solve this problem, we could use a version of binary search to test various floors of the building. If the egg breaks on that floor, we can adjust the test floor down by half the height. If the egg does not break, we can raise the test floor by half the remaining height.

When the algorithm finds the floor where the egg breaks, but does not break on the floor below it, it can return that as `f`.

An example algorithm might look like:

<br>

```
broken_eggs(n):
    current_floor = n/2

    if drop_egg(current_floor) == True and drop_egg(current_floor-1) == False:
        return current_floor

    elif drop_egg(current_floor) == True:
        current_floor = current_floor/2
    
    elif drop_egg(current_floor) == False:
        current_floor = (n-current_floor)/2
```

<br>

Like Binary Search, the run time of this algorithm is `O(log n)` in worst case scenario, because it is splitting up the searchable area in half on each iteration.
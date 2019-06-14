## Exercise I

#### a) O(n)

While this algorithm would not linearly run _every_ element between 0 and n (because it jumps by n^2 each time), the log time reduces to O(n), linear.


#### b) O(n) * O(n) * O(n) * O(1) = O(n^3)

The outer loop will run O(n), hitting every element between 0 and n.
The j nested loop will hit fewer elements (between 1 and n) but still runs lineary (O(n)).
The k nested loop will hit even fewer elements (between 2 and n) but still runs linearly (O(n)).
The l nested loops run constant time (between k+1 and k+10, or 10 loops each time), so evaluates to O(1)


#### c) O(n)

This recursive algorithm calls upon itself, which means it has to resolve itself down to the base case before returning an open call; but it only calls upon itself once each time, so the run time is still O(n)

## Exercise II




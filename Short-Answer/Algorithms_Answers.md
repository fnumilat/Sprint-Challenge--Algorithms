#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) Linear Time / O(n) - The running time increases linearly with the size of input data. It scales linearly with n. 

a = 0                  O(1)
while (a < n * n * n): O(n^3)
  a = a + n * n        O(n^2)

| n  |   n^3  |    n^2  | number of operations |
|----|--------|---------|----------------------|
| 6  |   216  |   36    |  6                   |
| 7  |   343  |   49    |  7                   |



b) O(n Log n) - There are 2 loops, one is nested inside the other one. The nested loop is dependent on "n" and increases exponentially so the time to reach "n" is halved. So instead of O(n^2) the complexity is O(n Log n).



c) Linear Time / O(n) - This time also increases linearly with the size of the input. If the input is 1, it will take less time to reach the base case of 0 and if the input is 500, it will take much longer since we are adding 2 and then substracting one with each recursive loop.

## Exercise II



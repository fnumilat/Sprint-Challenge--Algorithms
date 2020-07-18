# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```python
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```


```
b)  sum = 0
    for i in range(n):
      j = 1
      while j < n:
        j *= 2
        sum += 1
```

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```

## Exercise II

Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f. Devise a strategy to determine the value of f such that the number of dropped + broken eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode AND give the runtime complexity of your solution.

# # Going to implement Binary Search for this problem because it's clear that eggs are not breaking at the floors that are lower than f.
# # This way we only search the floors higher than f and we literally avoid half of the floors each time.

# # define a function which takes as parameters n floors
    # initialize a variable to hold the starting point for our search
        # this will be set to the first floor
    # initialize a variable to hold the ending point for our search
        # this will be set to the top floor
    
    # create a loop which will continue as long as our starting and ending points have not crossed over each other
       # define a midpoint between the current starting and ending values
       # if at the current floor eggs break, but at the floor below, they do not, we have found f and can return this floor number
       # if at the current floor eggs are not breaking, set the new start to be the former midpoint (plus one so we don't search the actual midpoint again) and the end stays the same. Continue searching.
       # if at the current floor eggs break, but at the floor below, they also break, we need to keep searching, but floor 'f' is below. Set the end to be the former midpoint -1 and continue searching.

Runtime is O(log n) for binary search, since we will never be searching through the whole array at any time. It will halve each iteration.

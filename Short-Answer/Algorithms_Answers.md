#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n) time. Although the while loop is n^3, since a grows by n^2 each time, 
we can divide n^3 / n^2, giving us n.


b) O(n log n). The outer for loop is O(n). Inside that for loop, 
we iterate through j exponentially, which is O(log N), so we multiply and get 
O(n log n) 


c) O(n), bunnies decrements by 1 each time until we hit the base case of 0.
n = number of bunnies

## Exercise II
All floors x < f will not break, and all floors x > f will break. So that means
in order the find the highest floor, we need to find an n such that floors x-1 doesnt break and x+1 breaks.
I would approach this with an algorithm similar to binary search. I would try the midpoint of the building first,
and if it breaks, that means the floor f is going to be less than the current midpoint. If it doesn't break, then f
is going to be higher. We move our pointers accordingly, ultimately cutting the available floors in half.
Repeat this process until we find floor f.
The time complexity is going to be O(log N), since we cut the amount of elements to search by half
each time.

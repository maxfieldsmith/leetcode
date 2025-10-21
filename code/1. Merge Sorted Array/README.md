As we iterate through the array we want to get the largest number between
the two lists. Since both lists are given in ascending order that means
that the last element in each list is the largest (for that list). Therefore,
if we do a reverse traversal we should grab the largest element from both arrays
and add it to the last (encountered) index of the resulting list.

```
      num1           num2
[1, 2, 3, 7, 8]   [3, 6, 9]
             ^  <        ^
      final
[ , , , , , , , 9]

      num1           num2
[1, 2, 3, 7, 8]   [3, 6, 9]
             ^  >     ^
        final
[ , , , , , , 8, 9]

      num1           num2
[1, 2, 3, 7, 8]   [3, 6, 9]
          ^     >     ^
        final
[ , , , , , 7, 8, 9]

      num1           num2
[1, 2, 3, 7, 8]   [3, 6, 9]
       ^        <     ^
        final
[ , , , , 6, 7, 8, 9]

      num1           num2
[1, 2, 3, 7, 8]   [3, 6, 9]
       ^        =<  ^
        final
[ , , , 3, 6, 7, 8, 9]

      num1           num2
[1, 2, 3, 7, 8]   [3, 6, 9]
       ^        
        final
[ , , 3, 3, 6, 7, 8, 9]

      num1           num2
[1, 2, 3, 7, 8]   [3, 6, 9]
    ^
        final
[ , 2, 3, 3, 6, 7, 8, 9]

      num1           num2
[1, 2, 3, 7, 8]   [3, 6, 9]
 ^
        final
[ 1, 2, 3, 3, 6, 7, 8, 9]
```
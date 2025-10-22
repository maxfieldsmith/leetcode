Keep track of where the last non-val element was located
Iterate through nums and if num is not val then insert in-place
where last non-val element was located

```
nums = [3, 2, 1, 3]    val = 3

not_val = 0

[3, 2, 1, 3]
 ^ == val so do nothing
    ^ != val so last non-val location becomes num
[2, 2, 1, 3] not_val = 1
       ^ != val so last non-val location becomes num
[2, 1, 1, 3] not_val = 2
          ^ == val so do nothing
return nums[:not_val] # nums[:2]
```
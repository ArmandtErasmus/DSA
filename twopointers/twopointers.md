# Two Pointers

The two pointers pattern uses (as the name suggests) two pointers $i$ and $j$ which reference the indices of an array/list. In general, we assume that the array is sorted in some way, and we assign the $i$ pointer to the first element in the array, and the $j$ pointer to the last element in the array. Then we move the $i$ pointer to the right and the $j$ pointer to the left based on some condition.

The pointers essentially iterate over an array. This pattern is useful when:
- You want to compare elements in a sorted array/list
- You want to rearrange/remove elements in-place
- You want to search for pairs in a sorted array (possibly to satisfy some condition)

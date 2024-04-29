# Two Pointers

The two pointers pattern uses (as the name suggests) two pointers $i$ and $j$ which reference the indices of an array/list. In general, we assume that the array is sorted in some way, and we assign the $i$ pointer to the first element in the array, and the $j$ pointer to the last element in the array. Then we move the $i$ pointer to the right and the $j$ pointer to the left based on some condition.

The pointers essentially iterate over an array. This pattern is useful when:
- You want to compare elements in a sorted array/list
- You want to rearrange/remove elements in-place
- You want to search for pairs in a sorted array (possibly to satisfy some condition)

Example:
Given a 1-indexed array of integers numbers that is already sorted in non-decreasing order, find two numbers such that they add up to a specific target number. Let these two numbers be numbers[index1] and numbers[index2] where 1 <= index1 < index2 <= numbers.length.

Return the indices of the two numbers, index1 and index2, added by one as an integer array [index1, index2] of length 2.

The tests are generated such that there is exactly one solution. You may not use the same element twice.

Your solution must use only constant extra space.

Solution:
```python
class Solution:
    def twoSum(self, numbers: List[int], target: int) -> List[int]:
        
        leftPtr = 0
        rightPtr = len(numbers) - 1

        while leftPtr < rightPtr:
            if numbers[leftPtr] + numbers[rightPtr] == target:
                return ([leftPtr + 1, rightPtr + 1])
            elif numbers[leftPtr] + numbers[rightPtr] < target:
                leftPtr += 1
            else:
                rightPtr -= 1
```

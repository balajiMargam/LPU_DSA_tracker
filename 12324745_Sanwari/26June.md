# h1p1  Quick Sort with Lemito Partition

- This code implements the Merge Sort algorithm. It recursively divides the array into smaller parts, sorts them, and then merges them back in ascending order. The overall time complexity is O(n log n)

```
python
class Solution:
    def sortArray(self, nums: List[int]) -> List[int]:

        def mergeSort(arr):
            if len(arr) <= 1:
                return arr

            mid = len(arr) // 2
            left = mergeSort(arr[:mid])
            right = mergeSort(arr[mid:])

            i = j = 0
            ans = []

            while i < len(left) and j < len(right):
                if left[i] < right[j]:
                    ans.append(left[i])
                    i += 1
                else:
                    ans.append(right[j])
                    j += 1

            return ans + left[i:] + right[j:]

        return mergeSort(nums)


```
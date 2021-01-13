# leetcode-cpp-exercise-everday

## 2021-1-13:Remove Duplicates from Sorted Array (26)
Given a sorted array nums, remove the duplicates in-place such that each element appears only once and returns the new length.
Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

```c++
// leetcode, remove duplicates from sorted array 
// time complex o(n)
class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        if (nums.empty()) return 0;

        int index = 0;
        for (int i = 0; i < nums.size(); i++){
            if (nums[index] != nums[i])
                nums[++index] = nums[i];
        }
        return index + 1;

    }
};

```



## 2021-1-13:  80. Remove Duplicates from Sorted Array II

Given a sorted array *nums*, remove the duplicates [**in-place**](https://en.wikipedia.org/wiki/In-place_algorithm) such that duplicates appeared at most *twice* and return the new length.

Do not allocate extra space for another array; you must do this by **modifying the input array [in-place](https://en.wikipedia.org/wiki/In-place_algorithm)** with O(1) extra memory.

```c++
class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        if (nums.size() <= 2) return nums.size();

        int index = 2;
        for (int i = 2; i < nums.size(); i ++){
            if (nums[i]!=nums[index -2])
                nums[index++] = nums[i];
        }
        return index;
    }
};
```


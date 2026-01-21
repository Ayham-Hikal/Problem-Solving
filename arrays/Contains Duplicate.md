# 🧩 Contains Duplicate (217)

## 📌 Problem Description

The goal of this problem is to check for duplicates in an integer array.

Traverse the array and verify whether any element has already appeared before.  
If a duplicate is found, return `true`. Otherwise, after checking all elements, return `false`.

## 💡 Approach

The idea is to detect duplicates while traversing the array only once.  
We use a **set** to keep track of numbers that have already been seen.

As we iterate through the array:
- If the current number already exists in the set, it means a duplicate is found, so we return `true`.
- Otherwise, we add the number to the set and continue.

If the loop finishes without finding any duplicates, we return `false`.

Using a set allows for fast lookup, making the solution efficient.

## 🧠 Algorithm Steps

1. Initialize an empty set to store visited elements.
2. Traverse each element in the array:
   - If the element is already in the set, return `true`.
   - Otherwise, add the element to the set.
3. If no duplicates are found after completing the loop, return `false`.

## 🔍 Solution

class Solution:
    def containsDuplicate(self, nums: List[int]) -> bool:
        result = set()
        for i in nums:
            if i in result:
                return True
            result.add(i)
        return False
 

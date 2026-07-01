# Data Structures & Algorithms

Problem-solving techniques, data structures, algorithms, and coding practice.

#Two Sum Problem
Array ,target value, print the index of elements whose sum is target value
def twoSum(nums: list[int], target: int) -> list[int]:
    # Dictionary to store the value and its corresponding index
    num_to_index = {}
    
    for index, num in enumerate(nums):
        complement = target - num
        
        # If the complement is already in the dictionary, return the indices
        if complement in num_to_index:
            return [num_to_index[complement], index]
        
        # Otherwise, store the current number and its index
        num_to_index[num] = index                                                               Time Complexity: O(n)

Brute Force Approach :: O(n^2)
n=int(input("Enter no of elemnets in your arr"))
t=int(input("enter target value"))
l=[]
for i in range(n):
  i=int(input())
  l.append(i)
for i in range(n):
  for j in range(i+1,n):
    if l[i]+l[j]==t:
      print([i,j])



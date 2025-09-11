- #Array #[[Two Pointer]] #[[Binary Search]]
- Goal
	- Given an array of numbers sorted in non-decreasing order find two numbers that add up to a given target. Return an array of the indices of these two numbers plus 1
- Thinking Behind the Algorithm
	- Lets start with a two pointer approach. We will have a left pointer starting at the 0 index of the numbers array and right pointer staring at the last value in the numbers array. We then can check whether the sum of the numbers at our pointers are equal, greater than, or less than. If they are equal we can return our left and right pointers in an array + 1. If they are greater than we can use the fact that the array is sorted in a non-decreasing order and just decrement our pointer, effectively decreasing the sum. The same applies to if the sum is less than except we increase the left pointer
- Implementation
	- [[Python Implementation]] #card
	  collapsed:: true
		- ```
		  class Solution:
		      def twoSum(self, numbers: List[int], target: int) -> List[int]:
		          l = 0
		          r = len(numbers) - 1
		  
		          while l < r:
		              s = numbers[l] + numbers[r]
		              if s == target:
		                  return [l + 1, r + 1]
		              elif s < target:
		                  l += 1
		              else:
		                  r -= 1
		  
		  ```
	- [[Javascript Implementation]] #card
	  collapsed:: true
		- ```
		  /**
		   * @param {number[]} numbers
		   * @param {number} target
		   * @return {number[]}
		   */
		  var twoSum = function(numbers, target) {
		      let l = 0;
		      let r = numbers.length - 1;
		      let sum = 0;
		  
		      while(l < r){
		          sum = numbers[l] + numbers[r];
		          if (target == sum){
		              return [l + 1, r + 1]
		          }else if (sum < target){
		              l += 1
		          }else{
		              r -= 1
		          }
		      }
		  };
		  ```
	- [[C++ Implementation]] #card
	  collapsed:: true
		- ```
		  
		  ```
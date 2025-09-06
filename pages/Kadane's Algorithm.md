- #[[Eponymous Algorithms]] #[[Dynamic Programming]]
- Definition
	- A dynamic programming algorithm for finding the maximum sub array of a larger array.
- Specification
	- In the algorithm we have a max_current and a max_global, both are initialized to the first value of the array then the Algorithm loops through the array setting max_current to the max between the current element or max_current + the current element. Set max_global to max_current if it is larger
- Implementation
	- ```
	  def kadanes_algorithm(arr):
	      if not arr:
	          return 0
	      
	      max_current = arr[0]
	      max_global = arr[0]
	  
	      for i in range(1, len(arr)):
	          max_current = max(arr[i], max_current + arr[i])
	  
	          if max_current > max_global:
	              max_global = max_current
	  
	      return max_global
	  ```
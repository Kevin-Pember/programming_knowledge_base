- #Python
- What are they used for
	- Used to describe what a function does and how to call it
	- Not limited to only python, other languages such as Lisp, Elixir, Clojure, Gherkin, Julia and Haskell support them
	- can be a
- Format
	- Single triple quotes ''' like these ''' or Double triple quotes """or these"""
	- They should start with a capital and end with a period
	- first line should be a summary of what the function does
	- second line should be a space separating first line from the rest
	- subsequent lines should describe calling conventions and more
- Project Formats
	- Googles's Format: [link](https://google.github.io/styleguide/pyguide.html)
		- ```
		  	"""
		      Multiplies two numbers and returns the result.
		  
		      Args:
		          a (int): The first number.
		          b (int): The second number.
		  
		      Returns:
		          int: The product of a and b.
		      """
		  ```
	- Numpydoc Format: [Link](https://numpydoc.readthedocs.io/en/latest/format.html)
		- ```
		      """
		      Divide two numbers.
		  
		      Parameters
		      ----------
		      a : float
		          The dividend.
		      b : float
		          The divisor.
		  
		      Returns
		      -------
		      float
		          The quotient of the division.
		      """
		  ```
-
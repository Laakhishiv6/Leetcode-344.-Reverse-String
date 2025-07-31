# Leetcode-344.-Reverse-String
# Description
Write a function that reverses a string. The input string is given as an array of characters s.

You must do this by modifying the input array in-place with O(1) extra memory.
# Solution
In order to reverse a string without using extra memory and rather just modifying the string . 

We can take 2 pointers left and right , where left is initialised as 0th index and right is initialised at the end of the array.

By swapping the values of left and right we can reverse the array , simultaneously increment the left pointer by 1 and decrement right ppinter by 1 .

array= ["L","A","A","K","H","I"]
         |                   |
        left               right

array= ["I","A","A","K","H","L"]
         |                   |
        left               right
array= ["I","H","A","K","A","L"]
             |           |
            left         right
array= ["I","H","K","A","A","L"]
                 |   |
                left right
reversed = ["I","H","K","A","A","L"]
                     |   |
                  LEFT  RIGHT 


# Algorithm
1. Initialise 2 pointers left and right as 0 and len(s)-1.
2. Use a while loop until left < right.
3. Swap the values of left and right.
4. Increment left with 1 and decrement right with 1 .
# Code
class Solution:

    def reverseString(self, s: List[str]) -> None:
        """
        Do not return anything, modify s in-place instead.
        """
        left=0
        right=len(s)-1
        while left<right:
            s[left],s[right]=s[right],s[left]
            left+=1
            right-=1
# Time Complexity
The while loop runs until the two pointers (left and right) meet.

Each iteration swaps two elements and moves the pointers inward.

Total number of swaps: n/2 for a list of length n.

Time Complexity: O(n)

Where n is the length of the input list s.

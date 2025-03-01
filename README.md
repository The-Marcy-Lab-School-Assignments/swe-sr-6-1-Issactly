# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Arrays, Linked Lists and Doubly Linked Lists all allow programmers to organize data in a sequence. So, how would you choose to use one over the other?

In your response, make sure to compare the time complexities for insertion, removal, and random access (grabbing a particular known element by index/position) for each data structure as well as memory usage and ease of traversal.

### Response 1


## Prompt 2

Imagine you are developing a web browser's "back" button functionality. When a user clicks "back," the browser should navigate to the previously visited webpage. 

Would you use a stack or a queue to implement this functionality? 

In your response, explain what a Stack/Queue is and why it would be best for this use case. Make sure that your response includes the terms LIFO or FIFO.

### Response 2

## Prompt 3

What is an Abstract Data Type and why are they worth learning about?

### Response 3

## Prompt 4

A few classic problems involving a stack are the `isBalanced` and `isPalindrome` functions. Choose one of these functions and provide a solution to it along with a brief lesson explaining how it works. 
-# Is this asking for a code example?

### Response 4
isBalanced is a classiv problem that checks if a given string is 'balanced'. For example the string '((()))' is balanced as it has a closing bracket for every opening one. One solution for this:

function isBalanced(str) {
  const stack = str.split('')
  const check = []
  
  while(stack.length) {
  
    let curr = stack.shift()
    
    if(check.length == 0) {
      check.push(curr)
    } else {
      if(check[check.length - 1] === '(' && curr === ')') {
        check.pop()
      } else {
        check.push(curr)
      }
    }
  }
  console.log(compare.length === 0)
};

  What this does is you begin by splitting the given string using the split method and storing those characters into a variable called 'stack' (Which places those characters into an array. After, you declare a variable called 'check' that holds an empty array. The while loop will continue to run *while* there are still characaters in the array, the shift method will remove and return the current character going one by one. If the check array is empty (like on the first index of the array) if it is then we push to curr to save that character for later comparrison. If its not empty we move to else, where we compare if the last character in check is the matching pair to curr and if it *is* we can pop that character from check. Essentially we repeat the process of matching and popping or finding singles and pushing. If at the end the length of the stack is *not* 0 we use the console.log to get a false displayed in the console. else its true.


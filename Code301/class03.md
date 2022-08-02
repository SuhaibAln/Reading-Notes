# What does .map() return?
A new arry with the same length of the original and changes the value accourding to new assignment we make 

___
# If I want to loop through an array and display each value in JSX, how do I do that in React?
using curly braces {} .

___
# Each list item needs a unique unique key.
___
# What is the purpose of a key?
Keys help React identify which items have changed, are added, or are removed.

___
[Source](https://reactjs.org/docs/lists-and-keys.html)

# What is the spread operator?
refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments.
___

# List 4 things that the spread operator can do.
- combine 2 arrays
- add new item to the array
- combine 2 objects
- spread the array into separate arguments
___

# Give an example of using the spread operator to combine two arrays.
`[..."🙂🙃😉😊😇🥰😍🤩!"] // Array(9) [ "🙂", "🙃", "😉", "😊", "😇", "🥰", "😍", "🤩", "!" ]

const hello = {hello: "😋😛😜🤪😝"}
const world = {world: "🙂🙃😉😊😇🥰😍🤩!"}

const helloWorld = {...hello,...world}
console.log(helloWorld) // Object { hello: "😋😛😜🤪😝", world: "🙂🙃😉😊😇🥰😍🤩!" } `
___

# Give an example of using the spread operator to add a new item to an array.
`const fewMoreFruit = ['🍉', '🍍', ...fewFruit]
console.log(fewMoreFruit) //  Array(5) [ "🍉", "🍍", "🍏", "🍊", "🍌" ]`
___

# Give an example of using the spread operator to combine two objects into one.
`const objectTwo = {world: "🐻"}
const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}
console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }
const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}
objectFour.laugh() // 😂😂😂😂😂 `
___

# In the video, what is the first step that the developer does to pass functions between components?
He created a function and passed state
___

# In your own words, what does the increment function do?
if the input name  equals  name in the constructor , it will increment the count by 1
___

# How can you pass a method from a parent component into a child component?
using props and passing the method to the child component
___

# How does the child component invoke a method that was passed to it from a parent component?
using this.props and method name
___

# Bookmark
[React Tutorial through ‘Declaring a Winner’](https://reactjs.org/tutorial/tutorial.html)
[React Docs - Lifting State Up](https://reactjs.org/docs/lifting-state-up.html)

## Things I want to know more about
- What is the purpose of a key in React?

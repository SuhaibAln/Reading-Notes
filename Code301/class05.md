# What is the single responsibility principle and how does it apply to components?
a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.
# What does it mean to build a ‘static’ version of your application?
building a version of our site that is not dynamic.(has no dynamic elements)that the user can interact with. and we should never use state or any other dynamic elements.
# Once you have a static application, what do you need to add?
We need to add state in order to add interactivity , we need to identify  which components should  owns states
# What are the three questions you can ask to determine if something is state?
- Is it passed in from a parent via props? If so, it probably isn’t state.
- Does it remain unchanged over time? If so, it probably isn’t state.
- Can you compute it based on any other state or props in your component? If so, it isn’t state.

# How can you identify where state needs to live?
- dentify every component that renders something based on that state.
- Find a common owner component (a single component above all the components that need the state in the hierarchy).
- Either the common owner or another component higher up in the hierarchy should own the state.
- If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.
-----------------------------------
# What is a “higher-order function”?
Functions that operate on other functions, either by taking them as arguments or by returning them,
# Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?
`
1.      function greaterThan(n) {
2.      return m => m > n;
3.      }
4.      let greaterThan10 = greaterThan(10);
5.      console.log(greaterThan10(11));
6.      // → true
`
It is taking a function as an argument and returning a function.
# Explain how either map or reduce operates, with regards to higher-order functions.
map and reduce operate on arrays.

## Things I want to know more about
reduce 
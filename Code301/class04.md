## What is a ‘Controlled Component’?
- An input form element whose value is controlled by React by combining input and textarea bt react it makes the  React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. 
## Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
we should wait to store the users responses from the form into state  because we want to make sure that the user has entered all the required information before we store it in state
## How do we target what the user is entering if we have an event handler on an input field?
event.target.value
## Why would we use a ternary operator?
less code is  more readable
## Rewrite the following statement using a ternary statement:
- if :
`if(x===y){
  console.log(true);
} else {
  console.log(false);
}`
- ternary:
`x===y ? console.log(true) : console.log(false)`
# Bokmark 
[React Bootstrap - Forms](https://react-bootstrap.github.io/forms/overview/)
[React Docs - conditional rendering](https://reactjs.org/docs/conditional-rendering.html)


## Things I want to know more about
Forms are a great way to collect data from the user.so i need to know how to use forms in react
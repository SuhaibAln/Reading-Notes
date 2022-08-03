# Functional Programming Concepts
# 1. What is functional programming?
## - Functional programming doesn't change the state of its data.

# 2. What is a pure function and how do we know if something is a pure function?
## Pure functions return the same result every time - for instance, they don't use global objects, instead passing that data as a parameter of the function. They also don't change the variables passed to them (so a "counter" function would return an incremented value but not change the original "count" value).

# 3. What are the benefits of a pure function?
Pure functions are predictable - we know how they'll behavee in different contexts. Using pure functions also reduces issues when you change other parts of your code.

# 4. What is immutability?
## - Immutable data can't change state; if you want to change it, create a new object.

# 5. What is Referential transparency?
## - Combining pure functions and immutable data leads to referential transparency - that is, the function will always produce the same result, because the data coming in & out doesn't change.

# Node.js
# 1. What is a module?
## - A module is a piece of code that has a single purpose (similar to a component).

# 2. What does the word ‘require’ do?
## - "Require" makes modules available in other parts of the project.

# 3. How do we bring another module into the file the we are working in?
## - require('[path to module]');

# 4. What do we have to do to make a module available?
## -module.exports = [function], where function is the function to be made available.

## Things I'd like to know more about
Benefits and drawbacks of this style vs. the style we've been using so far.
# Class 1

Insert "debugger" in JS file to create a break point. Step through in Chrome. Or click sidebar near line numbers to insert break point in Chrome.

callbacks = asyncronous - allows for failures

dsv = delimiter separated 
- d3 csv and tsv both just point to dsv for what delimiter to use

get parameters 
- refer to Code Academy API classes

JSON = JS object format

low dash

if indexOf returns -1 then it means the index is not present

Bower is part of Yeoman
- Yeoman = managed deployment process


# Class 2

d3 tooltip library.
- https://github.com/Caged/d3-tip

d3 Layouts
http://bl.ocks.org/mbostock/4062045

Layers are awesome in d3!

console.table(var)
- prints out a table view of an array

anounymous functions allow callbacks

# Class 3

c3.js is an easier framework for simple charts built on top of d3.
- http://c3js.org/gettingstarted.html

d3.set is a way to get only the unique values from an array

lodash has a lot nicer ways to handle data without converting it to a string like d3.
- allows method chaining like d3
- _.compact(exampleArray)
-- removes all the "falsey" values
--- null, "" (empty string), false, undefined
--- returns the cleaned up array
- _.intersection(array1, array2)
-- returns only the values that are in both arrays
- _.difference(array1, array2)
-- returns the unique values in array1 that are not in array2.
--- not the unique values in both

d3.map = returns a new array

try not to iterate over objects - key:values

=====
Post-Lunch

Looking at forcedPie example

_.countBy(object or array)
-- loops through and returns the count of the occurances. 

d3.extent = grabs the min and max of an array
-- handy way to get your domain

Mike Bostock forced layout talk
- amazing examples!
- https://vimeo.com/29458354
- http://mbostock.github.io/d3/talk/20110921/#0

Wrap the entire function in an anonymous function to reduce name space conflicts.

WKID = common placename ID

# Class 4
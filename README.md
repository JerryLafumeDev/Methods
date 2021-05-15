# String Methods


1. Length

not really a method its a property
returns a number on how many characters there is in a string.

ex.
"Hello".length  == 5
"".length == 0
" ".length == 1


2. Trim

removes big empty spaces of a string either at the beginning and/or the end of the string.
doesnt have any params

ex.
'   Hello world!   '.trim() == 'Hello World!'
'   Hello world!'.trim() == 'Hello World!'
'Hello world!   '.trim() == 'Hello World!'


3. Includes

searches inside of a string for a substring and returns true or false depending if that substring is inside the string you're looking for.

ex.
const string = "Hello world!"
const sub = "Hello"
string.includes(sub) // returns true

const sub2 = "hello"
string.includes(sub2) // returns false


3. indexOf

like includes in that this method searches a string for a substring but instead of returrning true or false it returns the index of where that substring is located in the string. 
if that substring isn't found in the string indexOf returns -1

ex.
const string = "Hello world!"
const sub = "H"
string.includes(sub) // returns 0

const sub2 = "o"
string.includes(sub2) // returns 4

const sub3 = "z"
string.includes(sub3) // returns -1


4. toUpperCase

returns that string with all upper case letters.

ex.
const string = "Hello world!"
string.toUpperCase() // returns "HELLO WORLD!"
"h".toUpperCase() // returns "H"

5. toLowerCase

returns that string with all lower case letters.

ex.
const string = "Hello world!"
string.toLowerCase() // returns "hello world!"
"H".toLowerCase() // returns "h"
"WORLD".toLowerCase() // returns "world"

6. replace
first param replace is what you want to replace in the form of a string or a regular expression
second param of replace is what you are replacing it with, either a string or a function

ex.
const string = "Hello world!"
string.replace("Hello", "Goodbye") // returns "Goodbye World!"
"H".replace(/h/g, "i") // returns "i"
"WORLD".replace("WORLD","SKY") // returns "SKY"

7. ChatAt

first param is index
returns the character of that index
if no index is listed it is defaulted to index 0

ex.
const string = "Hello world!"
string.chatAt(0) // returns "H"
"H".charAt(0) // returns "H"
"WORLD".charAt(2) // returns "R"

8. chatCodeAt

first param is index of the string
returns the UTF-8 code of that character

ex.
const string = "Hello world!"
string.chatAt(0) // returns "H"
"H".charAt(0) // returns "H"
"WORLD".charAt(2) // returns "R"

9. match

first param is a regular expression. 
returns an array of "matches" found inside the string
If you don't give any parameter and use the match() method directly, you will get an Array with an empty string: [""]

ex. 
const paragraph = 'The quick brown fox jumps over the lazy dog. It barked.';
const regex = /[A-Z]/g;
const found = paragraph.match(regex); // returns  ["T", "I"]

const paragraph2 = 'The quick brown fox jumps over the lazy dog. It barked.';
const regex2 = /T/g;
const found = paragraph2.match(regex2); // returns  ["T"]

const paragraph3 = 'The quick brown fox jumps over the lazy dog. It barked.';
const regex3 = /A/g;
const found = paragraph3.match(regex3); // returns  [""]


10. search

first param is a regular expression.
returns a number which represents the index of what is found
if nothing is found it will return -1

ex.
const paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';
const regex = /[^\w\s]/g;
paragraph.search(regex) // returns 43

const paragraph2 = 'The;
const regex2 = /T/g;
paragraph2.search(regex2) // returns 0

const paragraph3 = 'The;
const regex3 = /Z/g;
paragraph3.search(regex3) // returns -1


# Array Methods

1. Splice

 Swiss Army knife method can, add and delete in an  array
first parameter is index. a negative index just means start at the end of the array . -0 is the last element
second parameter is how many elements you want to delete
every parameter after those two are added to the array. arr.splice(0, 0, "hello", "world") adds hello world into the array


2. Slice

just like the string method also called slice that creates substring but instead it creates subarrays 
first and second param are indexes of the array, basically saying create another array from this index to that index.
    ( arr.slice(0, 3) = make a new array from index zero to index 3 )

negative index, means copy this many indexes from the end of the array tooo the end of the array. 
   ( arr.slice(-3) = means create a new array 3 indexes from the end  of the array to the end of the array. )
leaving slice empty is a way to make a copy of that array without any changes applied to it.


3. Concat

combines any object to an array , from other arrays, to variables or nested objects. and returns it all as an array.
can have as many params as you need , so you can combine as many things as you want.


4. forEach

allows to run a function for every element of the array, kind of like map or filter except forEach doesnt return a new array
you have to either write "function" before the params or use a fat arrow after your params. like this:
     arr.forEach(function(prams1, params2, params3) { blah })
     arr.forEach((parasm1, params2, params3) => { blahh })

the first param, is element, the second param is index and the third param is the array. 
   arr.forEach((element, index, array) => {
  alert(`${element} is at index ${index} in ${array}`);
})

you could also just put a function as the first param so that is runs the function for each element inside the array ! 
    arr.forEach(alert) = will alert each element as well


5. indexOf, lastIndexOf

indexOf and lastIndexOf, search through the array and returns the index of the element if its found inside the array. difference is that lastIndexOf searches from the end of the array instead of the beginning.
that being said the first params of these two is what element you're looking for.
the second param is "search starting from what index?"
if the element is not found in the array these two methods returns -1.
a minor issue is that these two methods can't use NaN


6. Includes

includes searches the array for an element and returns true or false if its found or not.
the first and only param of this method is "what element you're search for"


7. Split

split is a string method to turn a string into an array.
the first param of split is called the delimiter basically meaning what part of the string do you want to seperate the elements by. 

string.split() = turns the whole string as one big element inside the created erray.
["hello world!"]

string.split("") = turns every single letter and space into there own element inside the created array
["h", "e", "l", "l", "o", ....]

string.split(" ") = splits up the elements by every given space of the string inside the created array 
["hello", "world!"]

the second param of split is optional and its the amount of elements you want into the created array.
string.split(" ", 1) = only one element
["hello"] 


8. Join

join is an array method that turns the array into a string .
the first param is the "glue", basically what do you want seperating the elements when they become a string.
arr.join("-") = seperates all the elements with a -
"hello-world!"


9. Reduce / reduceRight

can go through each element of an array and return data, typically used to added all numbers of an array together. but you can use it for more.
the first param of reduce is "accumulator" basically this param is holding the result of the pervious outcome of the function call and also equals the intial value, if the intial value is provided. 
second param is the elements of the array.
third param is the indexes inside the array.
fourth param is the array itself.
you also have to use either "function" before the params or use a fat arrow
after you list what your function is doing with reduce if you put a comma after all that you can then decide what the "intial value" is .

arr.reduce((sum, current) => sum + current, 0)
here sum is the accumulator, current is the (current) element and 0 is the intial value.


10. Length

returns a number on how many elements are in the array.

# Object Methods

 1. Keys

first param is the object your are targetting, ( Object.keys(newObj) )
when used on an object with properties, it returns an array of that objects property names


2. Values 

first param is the object your are targetting, ( Object.values(newObj) )
when used on an object with properties, it returns an array of that objects property values


3. Entries

first param is the object your are targetting, ( Object.entries(newObj) )
when used on an object with properties, it returns a 2D array of that objects property names and values as pairs in side each sub array.


4. Assign

first param is the object your are targetting, ( Object.assign(newObj) )
second and every param after is an object that you want to combine with the first. if they have similar keys every keys that are the same will be raplced by the second objects key value pairs. 
it returns the updated object


5. Create

first param is the object your are targetting, ( Object.create(obj) )
returns a new object using the one passed in its params as a prototype.
used like this;
const newObj = Object.create(obj) 

6. Seal

first param is the object your are targetting, ( Object.seal(obj) )
returns the obj
new properties can not be added and existing properties can not be deleted
but if the properties are writable you can still change their values

7. Freeze

first param is the object your are targetting, ( Object.freeze(obj) )
returns the obj
new properties can not be added and existing properties can not be deleted and existing property's values can not be changed


8. DefineProperty

first param is the object your are targetting, ( Object.defineProperty(obj) )
second param is the property (key) you want to define / change
third param is an object { } with a property of "value" and its value and a property "writable" and its value as a boolean
if the second param is a property that already existed inside that object you will be able to see the change . but if it is not an existing property you won't be able to visibly see it but you can still access it with dot notation
depending if the property you changed / added is writable or not (true or false) you will / will not be able to re-assign it's value.  

9.DefineProperties

first param is the object your are targetting, ( Object.defineProperty(obj) )
second param is the property (key) you want to define / change as  an object { } with a property of "value" and its value and a property "writable" and its value as a boolean.
this method is like defineProperty but you can update / change multiple properties and it combines the second and third param
if the second param is a property that already existed inside that object you will be able to see the change . but if it is not an existing property you won't be able to visibly see it but you can still access it with dot notation
depending if the property you changed / added is writable or not (true or false) you will / will not be able to re-assign it's value. 



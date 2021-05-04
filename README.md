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

6. replace
first param replace is what you want to replace in the form of a string or a regular expression
second param of replace is what you are replacing it with, either a string or a function

7. ChatAt

first param is index
returns the character of that index
if no index is listed it is defaulted to index 0

8. chatCodeAt

first param is index of the string
returns the UTF-8 code of that character

9. match

first param is a regular expression. ex. ( /[A-Z]/g )
returns and array of anything that is found 

10. search



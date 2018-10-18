# Python String

In Python, Strings are arrays of bytes representing Unicode characters. However, Python does not have a character data type,
a single character is simply a string with a length of 1. Square brackets can be used to access elements of the string.

## Creating a String
Strings in Python can be created using single quotes or double quotes or even triple quotes.

String in single quotes cannot hold any other single quoted character in it otherwise an error arises because the compiler
won’t recognize where to start and end the string. To overcome this error, use of double quotes is preferred, because it 
helps in creation of Strings with single quotes in them. For strings which contain Double quoted words in them, use of 
triple quotes is suggested.Along with this, triple quotes also allow the creation of multiline strings.

## Example:

<pre>
# Python Program for 
# Creation of String 
  
# Creating a String  
# with single Quotes 
String1 = 'Welcome to the Singh World'
print("String with the use of Single Quotes: ") 
print(String1) 
  
# Creating a String 
# with double Quotes 
String1 = "I'm a Singh"
print("\nString with the use of Double Quotes: ") 
print(String1) 
  
# Creating a String 
# with triple Quotes 
String1 = '''I'm a Singh and I live in a world of "Singh"'''
print("\nString with the use of Triple Quotes: ") 
print(String1) 
  
# Creating String with triple 
# Quotes allows multiple lines 
String1 = '''Singh 
            For 
            Life'''
print("\nCreating a multiline String: ") 
print(String1) 

</pre>

## Output:

<pre>
String with the use of Single Quotes: 
Welcome to the Singh World

String with the use of Double Quotes: 
I'm a Singh

String with the use of Triple Quotes: 
I'm a Singh and I live in a world of "Singh"

Creating a multiline String: 
Singh
            For
            Life
            
    </pre>
    
   
   ## Accessing characters in Python:
   
In Python, individual characters of a String can be accessed by using the method of Indexing, to access a range of characters in the String, method of slicing is used. Slicing in a String is done by using a Slicing operator (colon). Indexing allows negative address references to access characters from the back of the String, e.g. -1 refers to the last character, -2 refers to the second last character and so on.
While accessing an index out of the range will cause an IndexError. Only Integers are allowed to be passed as an index, float or other types will cause a TypeError.


![string-indexing](https://user-images.githubusercontent.com/31289155/47180049-2dd1f380-d33d-11e8-9e44-2eb3e10ee691.jpg)


## Example:

<pre>
# Python Program to Access 
# characters of String 
  
String1 = "GeeksForGeeks"
print("Initial String: ") 
print(String1) 
  
# Printing First character 
print("\nFirst character of String is: ") 
print(String1[0]) 
  
# Printing Last character 
print("\nLast character of String is: ") 
print(String1[-1]) 
  
# Printing 3rd to 12th character 
print("\nSlicing characters from 3-12: ") 
print(String1[3:12]) 
  
# Printing characters between  
# 3rd and 2nd last character 
print("\nSlicing characters between " +
    "3rd and 2nd last character: ") 
print(String1[3:-2]) 
</pre>


## Output:
<pre>
Initial String: 
GeeksForGeeks

First character of String is: 
G

Last character of String is: 
s

Slicing characters from 3-12: 
ksForGeek

Slicing characters between 3rd and 2nd last character: 
ksForGee

</pre>

## Deleting/Updating from a String
In Python, Updation or deletion of characters from a String is not allowed. This will cause an error because item assignment or item deletion from a String is not supported. Although deletion of entire String is possible with the use of a built-in del keyword. This is because Strings are immutable, hence elements of a String cannot be changed once it has been assigned. Only new strings can be reassigned to the same name
## Example
#### Updation of a character:

<pre>
# Python Program to Update 
# character of a String 
  
String1 = "Hello, I'm a Singh"
print("Initial String: ") 
print(String1) 
  
# Updating a character  
# of the String 
String1[2] = 'p'
print("\nUpdating character at 2nd Index: ") 
print(String1)

</pre>

## Output:

#### Error:
<pre>
Traceback (most recent call last):
File “/home/360bb1830c83a918fc78aa8979195653.py”, line 10, in 
String1[2] = ‘p’
TypeError: ‘str’ object does not support item assignment

</pre>


## Example
#### Updating Entire String:

<pre>
# Python Program to Update 
# entire String 
  
String1 = "Hello, I'm a Singh"
print("Initial String: ") 
print(String1) 
  
# Updating a String 
String1 = "Welcome to the Singh World"
print("\nUpdated String: ") 
print(String1) 
</pre>

## Output:

<pre>
Initial String: 
Hello, I'm a Singh

Updated String: 
Welcome to the Singh World
</pre>

## Deletion of a character:

#### Example:
<pre>
# Python Program to Delete 
# characters from a String 
  
String1 = "Hello, I'm a Singh"
print("Initial String: ") 
print(String1) 
  
# Deleting a character  
# of the String 
del String1[2]  
print("\nDeleting character at 2nd Index: ") 
print(String1) 
</pre>

## Output:

#### Error:
<pre>
Traceback (most recent call last):
File “/home/499e96a61e19944e7e45b7a6e1276742.py”, line 10, in 
del String1[2]
TypeError: ‘str’ object doesn’t support item deletion

</pre>


## Deleting Entire String:
Deletion of entire string is possible with the use of del keyword. Further, if we try to print the string, this will produce an error because String is deleted and is unavailable to be printed.

## Example
<pre>
# Python Program to Delete 
# entire String 
  
String1 = "Hello, I'm a Geek"
print("Initial String: ") 
print(String1) 
  
# Deleting a String 
# with the use of del 
del String1  
print("\nDeleting entire String: ") 
print(String1)

</pre>

## Output:

#### Error:
<pre>
Traceback (most recent call last):
File “/home/e4b8f2170f140da99d2fe57d9d8c6a94.py”, line 12, in 
print(String1)
NameError: name ‘String1’ is not defined
</pre>


## Escape Sequencing in Python:
While printing Strings with single and double quotes in it causes SyntaxError because String already contains Single and Double Quotes and hence cannot be printed with the use of either of these. Hence, to print such a String either Triple Quotes are used or Escape sequences are used to print such Strings.
Escape sequences start with a backslash and can be interpreted differently. If single quotes are used to represent a string, then all the single quotes present in the string must be escaped and same is done for Double Quotes.
To ignore the escape sequences in a String, r or R is used, this implies that the string is a raw string and escape sequences inside it are to be ignored.


## Example:
<pre>
#Python Program for 
#Escape Sequencing  
#of String 
  
#Initial String 
String1 = '''I'm a "Geek"'''
print("Initial String with use of Triple Quotes: ") 
print(String1) 
  
#Escaping Single Quote  
String1 = 'I\'m a "Geek"'
print("\nEscaping Single Quote: ") 
print(String1) 
  
#Escaping Doule Quotes 
String1 = "I'm a \"Geek\""
print("\nEscaping Double Quotes: ") 
print(String1) 
  
#Printing Paths with the  
#use of Escape Sequences 
String1 = "C:\\Python\\Geeks\\"
print("\nEscaping Backslashes: ") 
print(String1) 
  
# Printing Geeks in HEX 
String1 = "This is \x47\x65\x65\x6b\x73 in \x48\x45\x58"
print("\nPrinting in HEX with the use of Escape Sequences: ") 
print(String1) 
  
# Using raw String to  
# ignore Escape Sequences 
String1 = r"This is \x47\x65\x65\x6b\x73 in \x48\x45\x58"
print("\nPrinting Raw String in HEX Format: ") 
print(String1) 
</pre>

## Output:
<pre>
Initial String with use of Triple Quotes: 
I'm a "Geek"

Escaping Single Quote: 
I'm a "Geek"

Escaping Double Quotes: 
I'm a "Geek"

Escaping Backslashes: 
C:\Python\Geeks\

Printing in HEX with the use of Escape Sequences: 
This is Geeks in HEX

Printing Raw String in HEX Format: 
This is \x47\x65\x65\x6b\x73 in \x48\x45\x58
</pre>


## Formatting of Strings:
Strings in Python can be formatted with the use of format() method which is very versatile and powerful tool for formatting of Strings. Format method in String contains curly braces {} as placeholders which can hold arguments according to position or keyword to specify the order.
A string can be left(<), right(>) or center(^) justified with the use of format specifiers, separated by colon(:). Integers such as Binary, hexadecimal, etc. and floats can be rounded or displayed in the exponent form with the use of format specifiers.

## Output:
<pre>
# Python Program for 
# Formatting of Strings 
  
# Default order 
String1 = "{} {} {}".format('Geeks', 'For', 'Life') 
print("Print String in default order: ") 
print(String1) 
  
# Positional Formatting 
String1 = "{1} {0} {2}".format('Geeks', 'For', 'Life') 
print("\nPrint String in Positional order: ") 
print(String1) 
  
# Keyword Formatting 
String1 = "{l} {f} {g}".format(g = 'Geeks', f = 'For', l = 'Life') 
print("\nPrint String in order of Keywords: ") 
print(String1) 
  
# Formatting of Integers 
String1 = "{0:b}".format(16) 
print("\nBinary representation of 16 is ") 
print(String1) 
  
# Formatting of Floats 
String1 = "{0:e}".format(165.6458) 
print("\nExponent representation of 165.6458 is ") 
print(String1) 
  
# Rounding off Integers 
String1 = "{0:.2f}".format(1/6) 
print("\none-sixth is : ") 
print(String1) 
  
# String alignment 
String1 = "|{:<10}|{:^10}|{:>10}|".format('Geeks','for','Geeks') 
print("\nLeft, center and right alignment with Formatting: ") 
print(String1) </pre>


## Output:
<pre>
Print String in default order: 
Geeks For Life

Print String in Positional order: 
For Geeks Life

Print String in order of Keywords: 
Life For Geeks

Binary representation of 16 is 
10000

Exponent representation of 165.6458 is 
1.656458e+02

one-sixth is : 
0.17

Left, center and right alignment with Formatting: 
|Geeks     |   for    |     Geeks|
</pre>


* Old style formatting was done without the use of format method by using % operator
## Example:
<pre>
# Python Program for 
# Old Style Formatting 
# of Integers 
  
Integer1 = 12.3456789
print("Formatting in 3.2f format: ") 
print('The value of Integer1 is %3.2f' %Integer1) 
print("\nFormatting in 3.4f format: ") 
print('The value of Integer1 is %3.4f' %Integer1) 
</pre>

## Output:
<pre>
Formatting in 3.2f format: 
The value of Integer1 is 12.35

Formatting in 3.4f format: 
The value of Integer1 is 12.3457
</pre>

## String constants:
<h4>BUILT-IN FUNCTION	      DESCRIPTION</h4>
<pre>

string.                       ascii_letters	Concatenation of the ascii_lowercase and ascii_uppercase constants.
string.ascii_lowercase	      Concatenation of lowercase letters
string.ascii_uppercase	      Concatenation of uppercase letters
string.digits	                Digit in strings
string.hexdigits	            Hexadigit in strings
string.letters	              concatenation of the strings lowercase and uppercase
string.lowercase	            A string must contain lowercase letters.
string.octdigits	            Octadigit in a string
string.punctuation	          ASCII characters having punctuation characters.
string.printable	            String of characters which are printable
String.endswith()	            Returns True if a string ends with the given suffix otherwise returns False
String.startswith()	          Returns True if a string starts with the given prefix otherwise returns False
String.isdigit()	            Returns “True” if all characters in the string are digits, Otherwise, It returns “False”.
String.isalpha()	            Returns “True” if all characters in the string are alphabets, Otherwise, It returns “False”.
string.isdecimal()	          Returns true if all characters in a string are decimal.
str.format()	                one of the string formatting methods in Python3, which allows multiple substitutions and value formatting.
String.index	                Returns the position of the first occurrence of substring in a string
string.uppercase	            A string must contain uppercase letters.
string.whitespace	            A string containing all characters that are considered whitespace.
string.swapcase()	            Method converts all uppercase characters to lowercase and vice versa of the given string, and returns it
replace()	                    returns a copy of the string where all occurrences of a substring is replaced with another substring.
</pre>


## Deprecated string functions:

#### BUILT-IN FUNCTION	      DESCRIPTION
<pre>

string.Isdecimal	            Returns true if all characters in a string are decimal
String.Isalnum	              Returns true if all the characters in a given string are alphanumeric.
string.Istitle	              Returns True if the string is a titlecased string
String.partition	            splits the string at the first occurrence of the separator and returns a tuple.
String.Isidentifier	          Check whether a string is a valid identifier or not.
String.len	                  Returns the length of the string.
String.rindex	                Returns the highest index of the substring inside the string if substring is found.
String.Max	                  Returns the highest alphabetical character in a string.
String.min	                  Returns the minimum alphabetical character in a string.
String.splitlines	            Returns a list of lines in the string.
string.capitalize	            Return a word with its first character capitalized.
string.expandtabs	            Expand tabs in a string replacing them by one or more spaces
string.find	                  Return the lowest indexin a sub string.
string.rfind	                find the highest index.
string.rindex	                Raise ValueError when the substring is not found.
string.count	                Return the number of (non-overlapping) occurrences of substring sub in string
string.lower	                Return a copy of s, but with upper case letters converted to lower case.
string.split	                Return a list of the words of the string,If the optional second argument sep is absent or None
string.rsplit()	              Return a list of the words of the string s, scanning s from the end.
rpartition()	                Method splits the given string into three parts
string.splitfields	          Return a list of the words of the string when only used with two arguments.
string.join	                  Concatenate a list or tuple of words with intervening occurrences of sep.
string.strip()	              It return a copy of the string with both leading and trailing characters removed
string.lstrip	                Return a copy of the string with leading characters removed.
string.rstrip	                Return a copy of the string with trailing characters removed.
string.swapcase	              Converts lower case letters to upper case and vice versa.
string.translate	            translate the characters using table
string.upper	                lower case letters converted to upper case.
string.ljust	                left-justify in a field of given width.
string.rjust	                Right-justify in a field of given width.
string.center()	              Center-justify in a field of given width.
string-zfill	                Pad a numeric string on the left with zero digits until the given width is reached.
string.replace	              Return a copy of string s with all occurrences of substring old replaced by new.

</pre>

# String slicing in Python to check if a string can become empty by recursive deletion
Given a string “str” and another string “sub_str”. We are allowed to delete “sub_str” from “str” any number of times. It is also given that the “sub_str” appears only once at a time. The task is to find if “str” can become empty by removing “sub_str” again and again.

## Examples:
<pre>
Input  : str = "GEEGEEKSKS", sub_str = "GEEKS"
Output : Yes
Explanation : In the string GEEGEEKSKS, we can first 
              delete the substring GEEKS from position 4.
              The new string now becomes GEEKS. We can 
              again delete sub-string GEEKS from position 1. 
              Now the string becomes empty.


Input  : str = "GEEGEEKSSGEK", sub_str = "GEEKS"
Output : No
Explanation : In the string it is not possible to make the
              string empty in any possible manner.
 </pre>
Recommended: Please try your approach on {IDE} first, before moving on to the solution.

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



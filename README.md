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


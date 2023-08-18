Modules and pip in Python!

Module is like a code library which can be used to borrow code written by somebody else in our python program. There are two types of modules in python:

Built in Modules - These modules are ready to import and use and ships with the python interpreter. there is no need to install such modules explicitly.
External Modules - These modules are imported from a third party file or can be installed using a package manager like pip or conda. Since this code is written by someone else, we can install different versions of a same module with time.
The pip command
It can be used as a package manager pip to install a python module. Lets install a module called pandas using the following command

pip install pandas

pip is like npm but for python

.py is file domain for python files

adding comments in python is done by adding # at the start of the sentence

#print("Hello world")

escape characters \n is used to print the sentence in a new line

multi line comment = put the sentence in 3 single quotes
'''my name is amaan'''

commenting and uncommenting in python is done by ctrl forward slash

how to print I am Amaan "Hello world" everyone with the double quotes

print("I am Amaan \"Hello World\" everyone")

here \" is the escape sequence characters

variations of print statement

Other Parameters of Print Statement
object(s): Any object, and as many as you like. Will be converted to string before printed
sep='separator': Specify how to separate the objects, if there is more than one. Default is ' '
end='end': Specify what to print at the end. Default is '\n' (line feed)
file: An object with a write method. Default is sys.stdout

print("hey",3,4)

print("hey",3,4,sep="~")

output will be hey~3~4

print("hey",3,4,end="005")

output will be hey34005

variables initialisation in python
a =3 ;
not int or string or char or other stuff at initialisation.
how to find the data type of a variable

type(a);

a = 1
b = True
c = "Harry"
d = None

how to make complex number using python

a=complex(3,4)

output = 3 + 4j

list: A list is an ordered collection of data with elements separated by a comma and enclosed within square brackets. Lists are mutable and can be modified after creation.

Example:

list1 = [8, 2.3, [-4, 5], ["apple", "banana"]]
print(list1)

Output:

[8, 2.3, [-4, 5], ['apple', 'banana']]

Tuple: A tuple is an ordered collection of data with elements separated by a comma and enclosed within parentheses. Tuples are immutable and can not be modified after creation.

Example:

tuple1 = (("parrot", "sparrow"), ("Lion", "Tiger"))
print(tuple1)

Output:

(('parrot', 'sparrow'), ('Lion', 'Tiger'))

dict: A dictionary is an unordered collection of data containing a key:value pair. The key:value pairs are enclosed within curly brackets.

Example:

dict1 = {"name":"Sakshi", "age":20, "canVote":True}
print(dict1)

Output:

{'name': 'Sakshi', 'age': 20, 'canVote': True}

- Addition 15+7 22

* Subtraction 15-7 8

- Multiplication 5\*7 35

** Exponential 5**3 5 raise to the power 3

/ Division 15/6 2.5

% Modulus 15%6 3

// Floor Division 15//6 2

how to give output in python

print("The value of", a, "+", 3, "is: ", a + b)

comma is just the replacement of + from java

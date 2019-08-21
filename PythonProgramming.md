# Python Programming

## Install Python in Windows

* Download the latest python version for windows from [Python Downloads](https://www.python.org/downloads/).
* Save the download in an folder in the system.
* Setup the enviornment variables. Copy the folder path where exe file is present and set that path in environment variables PATH.
* Verify if python is successfully installed : Open command prompt, give command python -V

## Install Python Editor - Pycharm or Pydev in Eclipse
Pycharm and Eclispe are IDE's to write and execute codes.
### Pycharm Installation
* Download the community version of Pycharm from [Pycharm download](https://www.jetbrains.com/pycharm/) and install the IDE
* Create a project 

### Pydev setup on Eclipse 
For writing python code in Eclipse, a plugin named 'PyDev' is needed.
PyDev is a third-party plug-in for Eclipse and features code refactoring, graphical debugging and analysis for programming in Python. 
* Install Eclipse
* Once Eclispse is installed, 
   * go to HELP -> Market Place
   * search for PyDev plugin. 
   * click on install button.
   * accept the linence and click on finish button
   * click on the certificate to accept
* Pydev installed successfully on eclispe
* Go to eclispe and see if the pydev is installed successfully
   click on File, you can see pydev module over there.

## Install Python PIP
PIP is a package management system used to intsall and manage software packages written in python.
pip.exe gets installed with the python. Give the path of pip executable file on enviroment variables.
*  Go to the location where python is installed
*  Go to the folder 'scripts' and check for pip.exe
*  Copy the location "../python/scripts" and set the path in environment variables

## Python Programming Basics
### Taking user input on runtime and printing it
The below program explains how to take user input in runtime and how to print it on console
program :

```python
i=input("Please enter your name -->")
print("Your name is -->" + i)
```
Program explanation:

* input method  to take user input and print method to print it.
* This programs promts for input on runtime it prints on console.

Program output :

```powershell
Please enter your name -->testing world
Your name is -->testing world
```

### Continuation symbol
Contination symbol is '\'(Backslash) which shows the program continues on the next line

Program :

```python
i=\
    input("Please enter your name -->")
print("Your name is -->" + i)
```

Program output :

```powershell
Please enter your name -->testing world
Your name is -->testing world
```

### Multiple statements in a line
Semicolon ; is used for writing multiple statements in a line
Program:

```python
i=input("Please enter your name -->");print("Your name is -->" + i)
```

Program output :

```powershell
Please enter your name -->testing world
Your name is -->testing world
```
### Condition Handling in Python
#### Conditional Handling: if - else
Program to demostrate if else conditional handling.
This program checks if a number is greater than 100 or not. The program prints GREATER if the given number is greater than 100 else print SMALLER

Program :

```python
i=101
if(i>100):
    print("GREATER")
else:
    print("SMALLER")
```
Program output:

```powershell
GREATER
```
Program to take a number from user and check if a number is greater than 100 or not. The program prints GREATER if the given number is greater than 100 else print SMALLER

Program:

```python
userNum=input("Please enter a number -->")
if(userNum>100):
    print("GREATER")
else:
    print("SMALLER")
```
This code throws an error, as the varible type of input number is not defined. 'userNum' is interperted as string. We need to typecast the input to integer.

Program output:

```powershell
Please enter a number -->101
Traceback (most recent call last):
  File "C:/Work/PyStudy/ConditionalHandling.py", line 12, in <module>
    if(userNum>100):
TypeError: '>' not supported between instances of 'str' and 'int'
```

Typecast string value to integer and run the above program again

Program :

```python
userNum=input("Please enter a number -->")
if(int(userNum)>100):
    print("GREATER")
else:
    print("SMALLER")
```

Program output:

```powershell
Please enter a number -->200
GREATER
```
### Multiple condition handling using if-elif-else
The below program explains multiple conditional handling using if-elif-else.
Takes an user number. Check if the number is negative. If not check if it is 0. If not check the number is positive. 
If positive check it is even number or odd

Program:

```python
userNum=input("Enter a number -->")
userNum=int(userNum) #typecasting string to int
if(userNum<0):
    print("This is negative number")
elif(userNum==0):
    print("Number is zero")
elif(userNum%2==0):
    print("Number is even")
else:
    print("Number is odd")
```

Program output:

```powershell
Enter a number -->21
Number is odd
```
It is not mandatory to write the 'else' on the last line in the above program. The below program also works.

```python
userNum=input("Enter a number -->")
userNum=int(userNum) #typecasting string to int
if(userNum<0):
    print("This is negative number")
elif(userNum==0):
    print("Number is zero")
elif(userNum%2==0):
    print("Number is even")
elif(userNum%2==1):
    print("Number is odd")
```
### Nested condition handling
Nested condition handling means conditions inside conditions .The below program explains nested if handling.
Program to take an user input.Check if the number is positive.If positive check if it is even or not.
program:

```python
userNum=input("Enter a number -->")
userNum=int(userNum) #typecasting string to int
if(userNum>=0):
 if(userNum%2==0):
    print("Number is even")
 else:
    print("Number is odd")
else:
    print("Number is negative")
```

program output:

```powershell
Enter a number -->45
Number is odd
```
### Condition handling with logical OR
If we have multiple conditions, if any of the condition become true the task will be performed.
This program explains logical OR condition. If the given number is less than zero or greater than 100, print the number is not between 0 and 100. Else print as number is between 0 and 100.
The syntax is :
```python
if (condition1 or condition2)
```
Program:

```python
userNum=input("Enter a number -->")
userNum=int(userNum)
if(userNum<0 or userNum>100):
    print("print the number is not between 0 and 100")
else:
    print("The number is between 0 and 100")
```
program output:

```powershell
Enter a number -->2
The number is between 0 and 100
```

```powershell
Enter a number -->102
The number is not between 0 and 100
```
### Conditional handling with logical AND
Logical AND condition means if both the conditions are true, the task will be performed.
This program explains logical AND condition. If the given number is greater than 0 or less than 100, print the number as invalid. Else print as valid number.
The syntax is :
```python
if (condition1 and condition2)
```
Program:

```python
#Take user input. If the number is >0 and <100, the number is between 1 and 100. Else the number is not between 1 and 100
userNum=input("Enter a number -->")
userNum=int(userNum)
if(userNum>0 and userNum<100):
    print("number is between 1 and 100")
else:
    print("number is not between 1 and 100")
```
program output:

```powershell
Enter a number -->2
number is between 1 and 100
```

```powershell
Enter a number -->102
number is not between 1 and 100
```
### Condition handling with NOT operator
The syntax is :
```python
if (input!=value)
```
Program:

```python
userNum=input("Enter a number -->")
userNum=int(userNum)
if(userNum!=100):
    print("The number is not 100")
else:
    print("The number is 100")
```

Program output:

```powershell
Enter a number -->200
The number is not 100
```
## Loops in Python
Whereever if a same task is needed to perform again and again, loops are used.
In loop we will have a starting point, then a condition check, then increment or decrement. Again goes for condition check. If condition is false, comes out of the loop
Two types loops handling in python
1. For loop
2. while loop
   
### For loop
For loop are of different formats.
1. For loop with final range
2. For loop with initial and final range
3. For loop with increment
4. For loop with decrement
5. For loop with list

#### For loop with final range
We are not giving initial range, only final range is provided. Whatever final range we give is excluded in output.
In the below program i=0 is set automatically and final range (10) is specified in the code. Hence print the numbers from 0 to 9

Program:

```python
#For loop with final range

for i in range(10):
    print(i)
```
The below program takes user input for the final range and print the numbers the range

Program:

```python
#For loop with final range

userNum=input("Enter a final range-->")
userNum=int(userNum)
for i in range(userNum):
    print(i)
```
Program output:

```powershell
Enter a final range-->6
0
1
2
3
4
5
```
#### For loop with inital and final range
Here we give inital and final range in for loop
The below example takes user input and give multiplication table of that number based on the initial and final range specified.
If user give input 7 and the initial range is 1 and final range is 6, it prints 7*1 = 7, 7*2 = 14, 7*3=21, 7*4=28 and 7*5=35.

Program:

```python
#For loop with inital and final range
userNum=input("please enter a number you need to multiply-->")
for j in range(1,6):
    print(userNum + " * " + str(j) + " = " + (int(userNum)*j))
```

Program output:

```powershell
please enter a number you need to multiply-->7
7 * 1 = 7
7 * 2 = 14
7 * 3 = 21
7 * 4 = 28
7 * 5 = 35
```
#### For loop with increment value
On previous for loops(For loops with final range and for loops with both inital and final range) increment was automatically going as 1. We can set our own increment value on for loop itself. 

Syntax
```python
for variable in range(inital value, final value, increment value)
```
Program:

```python
for i in range(1,11,2):
    print(i)
```
The above program prints from 1 to 10, by incrementing value by 2. Hence the output will be

Program output:

```powershell
1
3
5
7
9
```

#### For loop with decrement value
The decrement value is used when we need to run a reverse loop. Decrement value should be given as negative value.
Reverse loop syntax
```python
for variable in range(final value, initial value, decrement value)
```

The below reverse loop doesnot run, because if you run a reverse loop it is mandatory to give a third argument, to show the loop has to run in decrement order.

```python
    for j in range(10,1):
        print(j)
```
The initial range on the loop is excluded. The below program gives a reverse loop from 10 to 1.

Program:

```python
    for j in range(10,0,-1):
        print(j)
```

Program output:

```powershell
10
9
8
7
6
5
4
3
2
1
```
What happens if you give positive value for the decrement value
```python
    for j in range(10,0,1):
        print(j)
```
Nothing works as positive value means increase the value. Hence this is a reverse loop it does not work.

Program to print reverse table by taking number from the user

Program:

```python
#Program to print reverse multiplication table by taking number from the user

userNum=input("Enter the number which you need to multiply-->")
for i in range(10,0,-1):
    print(userNum + " * " + str(i) + " = " + str(int(userNum)*i))
```

program output:

```powershell
Enter the number which you need to multiply-->10
10 * 10 = 100
10 * 9 = 90
10 * 8 = 80
10 * 7 = 70
10 * 6 = 60
10 * 5 = 50
10 * 4 = 40
10 * 3 = 30
10 * 2 = 20
10 * 1 = 10
```

#### For loop with list
List is quite similar to array that we have seen in different programming languages to store data with different data types.
1. Create a list and print all values in the list

Program:

```python
#How to create and print list in python

list1=[1,2,'a','bcd','word','www.abc.com']
for i in list1:
    print(i)
```

Program output:

```powershell
1
2
a
bcd
word
www.abc.com
```
2. Another approach to treat a string as list and print it's characters

Program:

```python
for j in 'learning python':
    print(j)
```

Program output:

```powershell
l
e
a
r
n
i
n
g
 
p
y
t
h
o
n
```
3. Program to add numbers in a list
   
Program:

```python
#Add numbers in the list
list2=[10,20,30,40,50]
num=0
for k in list2:
    num=num+k

print("The sum of list is: " + str(num))
```
Note : the print statement should be written after a blank line. Else it will be treated inside the for loop. Here print statement should be outside of the loop.

Program output:

```powershell
The sum of list is: 150
```
### While loop
#### While loop with increments
Program to show while loop with increment value. This multiplies a given number as per the specified range

Program:
```python
#While loop with increments
userNum=input("Enter your number-->")
i=1
while(i<=10):
    print(int(userNum)*i)
    i+=1 # equal to i=i+1
```

Program output:
```powershell
Enter your number-->10
10
20
30
40
50
60
70
80
90
100
```

#### While loop with decrements
The program shows while loop with decrements. It prints the multipication of a given number in reverse order.

Program:

```python
#While loop with decrements
userNum2=input("Enter your number-->")
j=10
while(j>=1):
    print(int(userNum2)*j)
    j-=1 # equal to j=j-1
```

Program output:

```powershell
Enter your number-->10
100
90
80
70
60
50
40
30
20
10
```

## Break statements in python
Break is to come out of the loop from any condition. Once it comes out of the loop, it will not execute rest of the loop iteration.
Program to take a number from user and print the multiplication table. Anywhere the number generated after multiplying is 60, immediately break the problem

Program:

```python
userNum=input("please enter a number you need to multiply-->")
for i in range(1,10):
    if(int(userNum)*i==60):
        break
    print(int(userNum)*i)
```
The above program breaks when the result of multiplication is 60. 

program output:

```powershell
please enter a number you need to multiply-->10
10
20
30
40
50
```
## Continue statement
Continue is to skip the remaining part of the loop. For example in the above program the break statment breaks the loop and come out of it when result of multiplication is 60. When we use continue and check if the result of multiplication is 60, it skips the code to print 60 and execute the remaining iteration.

program:

```python
userNum=input("please enter a number you need to multiply-->")
for i in range(1,10):
    if(int(userNum)*i==60):
        continue
    print(int(userNum)*i)
```

Program output:

```powershell
please enter a number you need to multiply-->10
10
20
30
40
50
70
80
90
```
## Else Statement
When we are working on conditional handling we have seen else if. Here in python we can use else in looping as well. Else run after the loop execution ends.

Program:

```python
for i in range(1,11,2):
    print(i)
else:
    print("the loop ends")
```

Program output:

```powershell
1
3
5
7
9
the loop ends
```

## String Handling
### Fundamentals of string handling
String can be defined as a group of characters. In python strings can be placed in ' ' or " " or """ """
#### How to store strings
1. The string stored in single quotes
   
```python
data='learning python'
print(data)
```
2. The string stored in double quotes
```python
data="learning python"
print(data)
```
Both the program gives same output

Program output:

```powershell
learning python
```

3. If you want to store a string which has double quotes, you can give the entire string on single quotes

```python
data ='learn python from "www.abc.com"'
print(data)
```
Program output:

```powershell
learn python from "www.abc.com"
```
4. If you want to store a string which has single quotes, you can give the entire string on double quotes

```python
data ="learn python from 'www.abc.com'"
print(data)
```
Program output:

```powershell
learn python from 'www.abc.com'
```
5. If you want to store the strings in multiple lines

```python
data= """ 
My name is abc
I work as test lead
I lives in efgh
"""
print(data)
```

Program output:

```powershell
My name is abc
I work as test lead
I lives in efgh
```
#### Operator * to multiply strings
Operator * is used to display the string multiple times

```python
data= """ 
My name is abc
I work as test lead
I lives in efgh
"""
print(data * 3)
```

Program output:

```powershell
My name is abc
I work as test lead
I lives in efgh
 
My name is abc
I work as test lead
I lives in efgh
 
My name is abc
I work as test lead
I lives in efgh
```
#### Operator + is used for the concatenation of the string
Program to take name, address and profile from the user, concatenate and print in a readable sentence

```python
name=input("Please enter your name-->")
address=input("Please enter your address-->")
profile=input("Please enter your job-->")
print('Person ' + name + ' lives in ' + address + ' working as ' + profile)
```

Program output:

```powershell
Please enter your name-->abc
Please enter your address-->India
Please enter your job-->Test lead
Person abc lives in India working as Test lead
```
### Fetch substring
Common basic operations to fetch substring by index are
1. By giving index
2. By giving start and end index
3. Only staring index
4. Only end index

Program:

```python
data="learn python from www.abc.com"
#Fetch value from any index, just by passing an index.
#This prints the value on index 3, that is 'r'
print(data[3])

#Fetch substring by passing start and end index
#This prints the value from 6 to 12 index, that is 'python'
print(data[6:12])

#Fetch substring by passing only starting index
#This prints the value from 6th index onwards, that is 'python from www.abc.com'
print(data[6:])

#Fetch substring by passing only end index
#This prints the value up to 17th index, that is 'learn python from'
print(data[:17])
```
Program output:

```powershell
r
python
python from www.abc.com
learn python from
```
#### Pre-defined functions in string
1. Len - to find the length of a string. This a common function. This function is not specific to string.

```python
emailaddress="testing@abc.com"
#To fetch length of string
print(len(emailaddress))
```

Program output:
```powershell
15
```

All the below functions are string functions.Hence the syntax is 'string.functionname()'.

2. upper() - To convert the string to uppercase 
3. lower() - To convert the string to lowercase
4. capitalize() -To set first letter as capital

```python
emailaddress="testing@abc.com"
emailaddress1="TESTINGABC.COM"
#To convert the string to uppercase
#upper() function
print(emailaddress.upper())

#To convert the string to lowercase
#lower() function
print(emailaddress1.lower())

#To set first letter as capital
#capitalize() function
print(emailaddress.capitalize())
```
Program output:

```powershell
TESTING@ABC.COM
testingabc.com
Testing@abc.com
```
5. lstrip - To remove leading spaces in a string
6. rstrip - To remove trailing spaces in a string
7. strip - To remove both leading and trailing spaces

```python
#String with leading and trailing spaces
testaddress=" emailaddress@abc.com "
print(len(testaddress))# Here length is 22

#To remove leading spaces
# lstrip() function
print(len(testaddress.lstrip()))#After removing the leading space the length is 21

#To remove trailing space
#rstrip() function
print(len(testaddress.rstrip()))#After removing the leading space the length is 21

#To remove both the leading and trailing spaces
#strip() function
print(len(testaddress.strip()))#After removing both the leading and trailing spaces length is 20
```
Program output:

```powershell
22
21
21
20
```
8. Replace function- To find a part of string

```python
#Want to replace gmail with yahoo below
testemailaddress="testing@gmail.com"
print(testemailaddress.replace("gmail","yahoo"))
```

Program output:
```powershell
testing@yahoo.com
```

9. Find function - To find if a substring exits on a string. It returns the index of the substring if it is find. If not found it returns -1

```python
a="gmail"
print(testemailaddress.find(a)) #The result is 8(index of gmail)
b="gmail1"
print(testemailaddress.find(b))#The result is -1 as the substring is not present
```

Program output:
```powershell
8
-1
```
10. Split function - To break or split a string

```python
sentence="this is my email testing@gmail.com"
list1= sentence.split(" ")#whatever function coming out of split stores on list1. Here split the string with spaces
print(len(list1))#How many splits are present
print(list1)#display the split strings
```
Program output:
```powershell
5
['this', 'is', 'my', 'email', 'testing@gmail.com']
```
Programs based on the string functions
1. To find the occurence of a letter in a string
   In the below program three methods are explained

```python
#To find how many letter exits in a sentence
sentence="good morning how are you"
#To find the number of occurence of the letter 'o'
#first method
print("first method- Yes found prints as many times as the occurence of the letter")
for i in sentence:
    if(i=='o'):
        print("Yes found")

#second method - find the count
count=0
for j in sentence:
    if(j=='o'):
        count=count+1

print("Second method: the count is : " + str(count))

#third method using replace method
print(len(sentence))#Length is 23
#going to replace 'o' with nothing and find the length again
print(sentence.replace("o",""))#Here the length should be 23-5 = 18
x=len(sentence)
y=len(sentence.replace("o",""))
print("Third method : Occurence of 'o' is : " + str(x-y))
```

Program output:

```powershell
first method- Yes found prints as many times as the occurence of the letter
Yes found
Yes found
Yes found
Yes found
Yes found
Second method: the count is : 5
24
gd mrning hw are yu
Third method : Occurence of 'o' is : 5
```
2. Program to find the number of occurence of a word in a sentence

```python
sentence2="good morning have a good day"
#To find the number of occurences of word 'good'.We can use split function here
list1=sentence2.split(" ") #words split with spaces
print(list1)
wordcount=0
for k in list1:
    if(k=="good"):
        wordcount+=1
print("occurence of word 'good is : " + str(wordcount))
```
Program output:

```powershell
['good', 'morning', 'have', 'a', 'good', 'day']
occurence of word 'good is : 2
```

###How to compare two strings in python
1. If both are same case
   This program compares two strings and the result is both are same

```python
#Compare strings a and b.
a="testing"
b="testing"
if(a==b):
    print("same")
else:
    print("not same")
```

2.If both are case sensitive. Need to convert both of them to either upper case or lower case and then compare. The lower() or upper() method can be used. 

```python
f="Testing"
g="testing"
if(f.lower()==g.lower()):
    print("same")
else:
    print("not same")
```

3. If the string has leading or trailing spaces. First need to remove spaces in the string and then compare. Any function lstrip(), rstrip() or strip() can be used based on the strings.
   
```python
#Compare strings d and e. Hence spaces are present we need to remove the spaces first.
#Can use strip function
d="Testing"
e="Testing   "
if(d.strip()==e.strip()):
    print("same")
else:
    print("not same")
```

#### How to reverse a string
To reverse a string, declare another string as blank. Use for loop with decrement values as below
for variable in range(final value, initial value, decrement value)
    Final range should be the index of the last letter. To get this find length of the string and minus 1 from the length.
    Initial range should be 0, for that give the range -1, as the last value is excluded
    For descending order give the decrement value -1
Print the reverse letters to another string and print that string

```python
#Reverse a string
string1="testing"
#to reverse using one more string that is blank
string2=""
lenstring1=len(string1)
for i in range((lenstring1-1),-1,-1):
   #This prints the string in reverse order
    string2=string2+string1[i]
print(string2)
```

program output:

```powershell
gnitset
```
#### How to find if a string is palendrome or not
First reverse the input string and store in another string. Compare both the strings. If same it is a palendrome string.

```python
#To get user string and print if it is palendrome of not
userstring=input("enter the string-->")
luserstring=len(userstring)
revuserstring=""
for k in range((luserstring-1),-1,-1):
    revuserstring=revuserstring+userstring[k]

print(revuserstring)

if(userstring==revuserstring):
    print("palandrome")
else:
    print("not palandrome")
```

Program output:
```powershell
enter the string-->malayalam
malayalam
palandrome
```

## Complex data types
### List
1. List can hold multiple data(similar to array)
2. List is placed using square brackets[]
3. List can hold data of different data types
4. We can fetch data from list by passing index
5. We can update the data stored in the list
6. We can insert and delete data from the list, size will automatically increase or decrease
   
#### Fetch data from list by passing index
Data can be fetched from list by passing the index
1. By passing any index value - this returns the data on that particular index
2. By passing starting and end index - this returns the data with in start and end index
3. By passing only start index - this returns all the data in the list starting from the start index
4. By passing only end index - this returns all the data from the beginning till the end index

```python
list1=[23,43,55,"testing","python",'a','b',78,55]
#To fetch data by passing index
print(list1[2])

#To fetch data by staring and end index
print(list1[2:7])

#To fetch with start index only
print(list1[2:])

#To fetch with end index only
print(list1[:7])
```
Program output:

```powershell
55
[55, 'testing', 'python', 'a', 'b']
[55, 'testing', 'python', 'a', 'b', 78, 55]
[23, 43, 55, 'testing', 'python', 'a', 'b']
```
#### Update() function
Update function is to update data in the list. 

```python
list1=[23,43,55,"testing","python",'a','b',78,55]
#To update data in list
#To set 100 on third index
list1[3]=100 #The current third data 'testing' gets replaced by 100
print(list1)
```
program output:

```powershell
[23, 43, 55, 100, 'python', 'a', 'b', 78, 55]
```
Difference between insert and update function
Update replaces(updates) the current value on the specified index.
Insert inserts the specified value on the specified index to the list.

#### Insert and remove functions
Data can be inserted as well as removed
Program to explain insert() function. 

```python
list1=[23, 43, 55, 100, 'python', 'a', 'b', 78, 55]
#To insert data 'ABCD' on 3rd index
list1.insert(3,"ABCD")
print(list1)
```
Program output:
```powershell
[23, 43, 55, 'ABCD', 100, 'python', 'a', 'b', 78, 55]
```

Program to explain remove() function
Wherever the specified data is found, it removes from the list

```python
list1=[23, 43, 55, 'ABCD', 100, 'python', 'a', 'b', 78, 55]
list1.remove(55)
print(list1)
```
Program output:
```powershell
[23, 43, 'ABCD', 100, 'python', 'a', 'b', 78]
```
#### Len function 
To find the length of the list

```python
list1=[23, 43, 55, 'ABCD', 100, 'python', 'a', 'b', 78, 55]
print(len(list1)) #result is 10
```
#### cmp function to compare.
Note : This function run only on python 2 . On python 3 this gives an error

```python
lista=[23,89,"abc","testing",90,"python"]
listb=["good","morning",1,2,3]
cmp(lista,listb)
```
#### Concatenate the strings
+ operator is used for concatenating the strings

```python
lista=[23,89,"abc","testing",90,"python"]
listb=["good","morning",1,2,3]
listc=lista+listb
print(listc)
```
Program output:

```powershell
[23, 89, 'abc', 'testing', 90, 'python', 'good', 'morning', 1, 2, 3]
```
## Tuple in python
1. Tuples are quite similar to list, it can hold multiple data of different data types
2. Tuples are placed in (),seperated by comma
3. In tuple, we cannot change any value, also we cannot increase or decrease the size of the tuple
4. Fetch elements of tuple in same way as we are doing in list
5. Fetch length of tuple in same way as we are doing in list

Program to find length of a tuple and to fetch value in tuple by passing index

```python
tuple1=(12,34,"testing","www.abc.com","testing",23.4)
#Fetch length of the tuple. Same len function as in list
print(len(tuple1))
#Fetch data from tuple,same like list
#Fetch by passing index
print(tuple1[2])
```
Note: Once assigned any value to the tuple we cannot reassign any value.We cannot change any value in tuple.
The below code of assigning a value to the specified index to a tuble, gives TypeError: 'tuple' object does not support item assignment.

```python
tuple1[2]="ABCD"
```

#### Difference between a list and tuple
1. List is mutable where as tuple is immutable
  Mutable means the values in the list can be changed. Immutable means values in the tuples cannot be changed
2. On list data insertion and deletion are possible.Hence we can increase size of a list or decrease it. 
   In tuple insertion and deletion is not possible, hence cannot increase size of a tuple
3. List is placed in square brackets[], where as tuple is placed in parentheses

#### Count how many times a value is displayed in a tuple
Count function is used to count the occurence of a value in tuple.

```python
tuple1=(12,34,"testing","www.abc.com","testing",23.4)
print(tuple1.count("testing"))
```
#### Find index of any value in the tuple
Index function is used to fetch index of any value in the tuple

```python
tuple1=(12,34,"testing","www.abc.com","testing",23.4)
#To find the index of value '34'
print(tuple1.index(34)) #The result should be 1
#To find the index of the value 'testing'. If same value present in tuple multiple times, the first index where it is stored will display
print(tuple1.count("testing")) #The result should be 2
#If value is not present in tuple gets ValueError: tuple.index(x): x not in tuple
print(tuple1.index("python"))
```
#### Merge 2 tuples
To merge two tuples, + operator is used.Same as concatenation in list

```python
tuple1=(12,34,"testing","www.abc.com","testing",23.4)
tuple2=(100,200)
tuple3=tuple1+tuple2
print(tuple3)
```
Program output:

```powershell
(12, 34, 'testing', 'www.abc.com', 'testing', 23.4, 100, 200)
```

#### Display all values in the tuple
Two methods can be used
First method

```python
tuple1=(12,34,"testing","www.abc.com","testing",23.4)
for i in tuple1:
    print(i)
```

Second method

```python
tuple1=(12,34,"testing","www.abc.com","testing",23.4)
l=len(tuple1)
for j in range(0,l): #final range is the length of the tuple
    print(tuple1[j])
```

Program output:

```powershell
12
34
testing
www.abc.com
testing
23.4
```

## Dictionary in python
1. Stores value in the form of key value pair
2. placed inside curly brackets {}
3. key must always be unique
4. key and value could be of any data type
5. value can be fetched by passing its key
6. Dictionary keys are case sensitive- Same key name but with the different case are treated as different keys in Python dictionaries.
7. We can update any exiting value on the dictionary 
8. We can insert and delete items from dictionary

Difference between tuple and dictionary in python
1. Tuple is placed inside in () and it holds multiple data of multiple data type
   Where as dictionary is placed in {} and data is stored in the form of key-value pair.Keys should be unique. Keys and values can be of any data type
2. Values from tuple are fetched by using numeric value(index),where as in dictionary values are fetched by passing the key
3. Tuples are immutable that we cannot update, insert or delete any data from tuple.Its size cannot be incresed or decreased. Where as dictionaries are mutable , we can update, insert and delete items from the tuple. Hence the size of tuple can be increased or decreased.

### Declaring a dictionary
Data is stored as key value pair. Key and value is seperated by colon: and different data are seperated by comma ,
Key and value can be of any data type

```python
dic={"K1":"Val1",2:"val2","k3":"val3"}
print(dic)
```

Program output:

```powershell
{'K1': 'Val1', 2: 'val2', 'k3': 'val3'}
```
On the  dic, try to enter any value with duplicate key. On inserting an existing key with new value,it will update the existing value for that key

```python
dic2={"k1":"val1","k2":"val2","k3":"val3","k1":"34"} #insert k1 key again with another value
print(dic2)
```
Program output:

```powershell
{'k1': '34', 'k2': 'val2', 'k3': 'val3'}
```
### Fetch data from dictionary by passing key
To fetch value, we need to pass the key

```python
dic={"K1":"Val1",2:"val2","k3":"val3"}
print(dic["K1"]) #Fetch the value Val1 stored in the key K1
print(dic[2]) #Fetch the value  val2 stored in the key 2
```
Program output:

```powershell
Val1
val2
```
### Update data in dictionary
We can update the value for a particular key in dictionary
First method:

```python
dic={"K1":"Val1",2:"val2","k3":"val3"}
dic["k3"]="testing"
print(dic) # Previous value of k3 is reassigned with the new value
```
Program ouput:

```powershell
{'K1': 'Val1', 2: 'val2', 'k3': 'testing'}
```

Second method:
use update function

```python
mydic={"k1":"val1","k2":"val2","k3":"val3","k4":"val4"}
#using update function update the value in k3
mydic.update({"k3":"python"})
print(mydic)
```
program output:

```powershell
{'k1': 'val1', 'k2': 'val2', 'k3': 'python', 'k4': 'val4'}
```
### Insert values in to dictionary
We can add new data to dictionary
First method:

```python
dic={"K1":"Val1",2:"val2","k3":"val3"}
dic["k4"]="python" # A new key k4 is added with the value python
print(dic)
```
program output:

```powershell
{'K1': 'Val1', 2: 'val2', 'k3': 'testing', 'k4': 'python'}
```
Second method:
Using update function

```python
mydic={"k1":"val1","k2":"val2","k3":"val3","k4":"val4"}
mydic.update({"k5":"val5"}) # a new key k5 is added with value val5
print(mydic)
```

Program output:

```powershell
{'k1': 'val1', 'k2': 'val2', 'k3': 'val3', 'k4': 'val4', 'k5': 'val5'}
```
### Delete items from the dictionary
Delete can be done by passing key and by uisng del method

```python
mydic={"k1":"val1","k2":"val2","k3":"val3","k4":"val4"}
del mydic["k4"] #it deletes the key-value pair
print(mydic)
```
Program output:

```powershell
{'k1': 'val1', 'k2': 'val2', 'k3': 'val3'}
```
### Methods used in the dictionary
1. Keys
   Keys method prints all the keys from the dictionary
2. values
   values method prints all the values from the dictionary
3. items
   items method prints all the items, that is both the keys and values from the dictionary

```python
mydic={"k1":"val1","k2":"val2","k3":"val3","k4":"val4"}
print(mydic.keys())
print(mydic.values())
print(mydic.items())
```
Program output:

```powershell
dict_keys(['k1', 'k2', 'k3', 'k4'])
dict_values(['val1', 'val2', 'val3', 'val4'])
dict_items([('k1', 'val1'), ('k2', 'val2'), ('k3', 'val3'), ('k4', 'val4')])
```
### Len method to find the length of dictionary

```python
mydic={"k1":"val1","k2":"val2","k3":"val3","k4":"val4"}
print(len(mydic)) #it prints the length as 4
```

### Nested Dictionary
Dictionary inside the dictionary
In previous section we have seen how to write a dictionary and fetch data from it. In dictionary the data is stored as key value pair
```python
dic={'k1':'val1','k2':'val2','k3':'val3'}
```

When you place another dictionary in value part of the above dictionary it is nested dictionary
```python
NestedDic={'k1':{'k11':'val11'},
           'k2': {'k22':'val22','k23':'val23','k24':'val24'},
           'k3':'val3'}
```

Program to perform actions on nested dictionary
```python
NestedDic={'k1':{'empid':'1000','Name':'Sara'},
           'k2': {'empid':'2000','Name':'anna','profile':'tester'},
           'k3':{'empid':'3000'}}
print(NestedDic)

#Fetch data from nested dictionary
#To get the value inside the main dictionary
print(NestedDic['k1'])
#To get the value from sub dictionaries
#Pass the key value of the main dictionary and sub dictionary to fetch the data
print(NestedDic['k1']['Name'])
print(NestedDic['k2']['profile'])
print(NestedDic['k3']['empid'])
```

Program output:
```powershell
{'k1': {'empid': '1000', 'Name': 'Sara'}, 'k2': {'empid': '2000', 'Name': 'anna', 'profile': 'tester'}, 'k3': {'empid': '3000'}}
{'empid': '1000', 'Name': 'Sara'}
Sara
tester
3000
```

```python
NestedDic={'k1':{'empid':'1000','Name':'Sara'},
           'k2': {'empid':'2000','Name':'anna','profile':'tester'},
           'k3':{'empid':'3000'}}
print(NestedDic)
Adding data to dictionary
#To main dictionary
NestedDic['k4']={'empid':'4000','Name':'Elsa'}
print(NestedDic)
#To sub dictionary.
NestedDic['k3']['Name']="Dora"
NestedDic['k3']['profile']="Developer"
print(NestedDic)

#Update value to dictionary
NestedDic['k2']['profile'] = 'manager'
print(NestedDic)
```

Program output:

```powershell
{'k1': {'empid': '1000', 'Name': 'Sara'}, 'k2': {'empid': '2000', 'Name': 'anna', 'profile': 'tester'}, 'k3': {'empid': '3000'}}
{'k1': {'empid': '1000', 'Name': 'Sara'}, 'k2': {'empid': '2000', 'Name': 'anna', 'profile': 'tester'}, 'k3': {'empid': '3000'}, 'k4': {'empid': '4000', 'Name': 'Elsa'}}
{'k1': {'empid': '1000', 'Name': 'Sara'}, 'k2': {'empid': '2000', 'Name': 'anna', 'profile': 'tester'}, 'k3': {'empid': '3000', 'Name': 'Dora', 'profile': 'Developer'}, 'k4': {'empid': '4000', 'Name': 'Elsa'}}
{'k1': {'empid': '1000', 'Name': 'Sara'}, 'k2': {'empid': '2000', 'Name': 'anna', 'profile': 'manager'}, 'k3': {'empid': '3000', 'Name': 'Dora', 'profile': 'Developer'}, 'k4': {'empid': '4000', 'Name': 'Elsa'}
```

## Functions in python
Functions can be defined as a group of task to perform a particular task.
Function adavantages:
1. Functions bring re-usability.Write a code once and execute it as many items you want.
2. Decrease lot of duplicacy
3. It brings modularity in code, modularity means complete code is written in small chunks, wherever required that can be called
4. Easy for the team together in a code. 

### Declaring a function and calling it
def keyword is used to create a function in python
Function in Python is defined by the "def " statement followed by the function name and parentheses ( () )
syntax is

```python
def functionname():
    function body
```
Function body starts after the colon.
Since python works with indentation, body of the function cannot start from the same indentation of the function name. It shpuld start from the next indendation

Once function is declared we need to call it.

```python
def testing():
    print("This is testing function")
    print("just to print")
testing() #Calling the function
```

Program output:

```powershell
This is testing function
just to print
```
### Rules to create a function
1. Function body starts with colon :
2. All the code written with same indentation of the first line of the function are treated as function body
3. def keyword is used to create the functions
4. first line of function is optional,can be used for commenting
5. return keyword shows end of the function

```python
def hello():
    "the first line of function is optional and can be used for commenting.The # mark is not needed"
    print("first line of the function") # All the code with same indentation of the first line are considered inside function
    print("second line of the function")
    return # means end of the function
    print("after return")#this does not execute as return means end of the function

hello()
```
Program output:

```powershell
first line of the function
second line of the function
```
### Different types of functions
1. Functions not taking any argument and not taking any return value
2. Functions taking some argument but not return value
3. Functions taking no arguments but some return value
4. Functions taking both argument and return value

### Function with no argument and return value

```python
def welcome():
    print("hello..welcome")
welcome()
```

Program output:

```powershell
hello..welcome
```
### Function with arguments but no return value
Sum of two numbers

```python
def sum(a,b):
    c=a+b
    print("sum of two numbers: " + str(c))

sum(10,20) #here you can pass any value to add
```

Program output:

```powershell
sum of two numbers: 30
```
### Function with arguments and return value
Return command in Python specifies what value to give back to the caller of the function.
Suppose I want to perform (4*20)+10. How many functions are needed. Answer could be 1.This is correct answer if i am the only person who is using the code.If multiple persons are coding and code reusability is needed we can write it as two functions. one function to multiply and one function to addition.Multiplication function can be reused in addition function. In this kind of scenario where you want to reuse the code,concept of return comes to picture.

```python
def multiply(a,b):
    c=a*b
    return c

def addition(a,b):
    c=a+b
    print("The result is: "+str(c))

x=multiply(4,20) #call multiply function and store in a variable
addition(x,10) #reuse the multiply function
```

Program output:

```powershell
The result is: 90
```
### Function with no arguments and but return value

```python
def readdata():
    a=100
    return a

x=readdata()
print("print the return value: "+ str(x))
```
Program output:

```powershell
print the return value: 100
```
### Different types of arguments
The argument is a value that is passed to the function when it's called.
Arguments are declared in the function definition. While calling the function, you can pass the values for that arguments
1. Required arguments
When it is mandatory to pass the arguments, it is called required arguments.

```python
def takerequiredargument(a,b):
    c=a+b
    print("sum of the values: "+str(c))

takerequiredargument(10,20)
```
Program output:

```powershell
sum of the values: 30
```
Note : On the above function if you pass only one argument while calling the function it throws missing argument error

2. Keyword arguments
   When a function is called, we can pass values to the argument names.
   
```python
   def takekeywordargument(a,b):
    c=a+b
    print("sum of the values: "+str(c))

takekeywordargument(b=10,a=20)
```
Program output:

```powershell
sum of the values: 30
```

3. Default arguments
To declare a default value of an argument, assign it a value at function definition.

```python
def takedefaultargument(a,b=10):
    c=a+b
    print("sum of the values: "+str(c))

takedefaultargument(100) #Here  a gets the value of 100 as b value is set on function declaration itself
takedefaultargument(100,200) #Here a gets the value 100 and b gets the value 200
```

Program output:

```powershell
sum of the values: 110
sum of the values: 300
```
Default arguments should always define at the end.
The below program throws syntax error SyntaxError: non-default argument follows default argument

```python
def takedefaultargument1(a=10,b):
    c=a+b
    print("sum of the values: "+str(c))

takedefaultargument1(100)
```
Note : default arguments must be defined always in the end. or if you have defined any default argument all the arguments which are placed after that should have default values

Code that works
```python
def takedefaultargument(a=10,b=10) #non-default arguments should not follow the default arguments
def takedefaultargument(a,b=10)#default arguments should always define at end
def takedefaultargument(a,b=10,c=100)#non-default arguments should not follow the default arguments
def takedefaultargument(a,b,c=100)#non-default arguments should not follow the default arguments or default arguments should always define at the end
```
Code which throws error
```python
def takedefaultargument(a=10,b) #default arguments should always define at end
def takedefaultargument(a,b=10,c)#non-default arguments should not follow the default arguments
```
4.Multiple arguments
Multiple Arguments can also be passed as an array. Here in the example we call the multiple args (1,2,3,4,5) by calling the (*args) function.
We declared multiple args as number (1,2,3,4,5) when we call the (*args) function; it prints out the output as (1,2,3,4,5)

```python
def takemultiplearguments(*args):
    print(args)

takemultiplearguments(1,2,3,4,5)
```
Program output:

```powershell
(1, 2, 3, 4, 5)
```

## Class in Python
1. Python is a object oriented scripting lanuage. Python supports OOPS programming.
2. We can write our code in class
3. Class is a logical group of data and functions
4. Class can have variables,constants,functions and constructors
5. We can access class member by creating object of the class

### Steps to create a class and object
1. First create a class
   Syntax
   ```python
   class classname
   ```
2. Inside class, write class function. When creating a function inside the class, the first argument is automatically set with the name self.
3. To call any member of the class, create object of the class
   Syntax
   ```python
   obj=classname()
   ```
4. Once you have created object,call functions of the class by using the object
   
```python
class firstClass:
    def firstFunction(self):  #function inside the class.
        print("This is call function") #Inside function , something to print

obj=firstClass() #obj of class is created
obj.firstFunction() #call the function
```

Program output:
```powershell
This is call function
```
### Different type of functions inside the class
1. Function with no argument and no return value
2. Function with argument but no return value
3. Function with argument and return value

Program to explain different type of functions inside the class

```python
class Example:
    #Function with no argument and no return value
    def functionNoArgReturn(self):
        print("This is function with no arg and return")

    #Function which will take two argument,but no return value
    def sum(self,a,b):
        c=a+b
        print("sum is: "+str(c))

    #Function which will take argument and return value as well
    def multiply(self,a,b):
        c=a*b
        return c

obj=Example() #object of the class is created
obj.functionNoArgReturn() # Call the first function with no argument and return value
obj.sum(10,20) # call the second function with arguments
x=obj.multiply(10,20) # call the third function with arguments and return value
print("Multiplication is: "+str(x))
```
Program output:

```powershell
This is function with no arg and return
sum is: 30
Multiplication is: 200
```
## Constructors
1. Constructor is a special type of method
2. Created with __init()__, first argument is always self
3. Automatically called when object is created
4. Can take arguments
5. Constructor never returns any value
6. Constructors are used for initialization

Note : Unlike Java or C++, we cannot define multiple constructors in python.
### Create a constructor inside class
Constructor calls automatically when the object of the class is created

```python
class Example:
    #Create a constructor with no arguments
    def __init__(self):#Constructor body started
        print("This is a constructor")

    #Create a function
    def functionExample(self):
        print("This is a function")

obj=Example() #object of the class is created
#constructor calls automatically when the object of the class is created

obj.functionExample() #Function is called
```
Program output:

```powershell
This is a constructor
This is a function
```

### Create constructor with arguments
Constructor can take arguments. When an object of class is created, constructor is automatically called. On object creation itself pass the arguments to call the constructor

```python
class Example:
    #Create a constructor with arguments
    def __init__(self,a,b):#Constructor body started
        print("This is a constructor with arguments")
        c=a+b
        print("Sum of two numbers: " + str(c))

    #Create a function
    def functionExample(self):
        print("This is a function")

 #object of the class is created
#constructor calls automatically when the object of the class is created
obj=Example(10,20) #passing arguments to constructors

obj.functionExample() #Function is called
```

Program output:

```powershell
This is a constructor with arguments
Sum of two numbers: 30
This is a function
```
### Why and where we use constructors
 Whatever the code we want to execute at the start, that kind of code we need to place in constructor.That is constructors are used for initilization
 Example:
 Suppose 3 developers are working on a project. Each one has to write a method to get data from database A,B and C in a class
 Class -> class Database
 Dev1 -> writes the function to get data from database A, say getdataFromA
 Dev2 -> writes the function to get data from database B, say getdataFromB
 Dev3 -> writes the function to get data from datbase C, say getdataFromC
 For running the it, code to connect with database is needed. If the connection code is written in all three function, while running the code, each time connection estabilizes and hence duplicacy happens.
 If any one write in their method say in getdataFromB, other methods fails as the connection is not established.
 In this case, write the connenction code inside constructor. Hence it runs automatically when the object of the class is created.

 ## Create object of the class in another python file
 We can write class in one file and using another file we can create object for that class
 First we need to import python file to the file where we are creating the object
 Then create object of the class and use it

Create a python file 'ClassInOneFile.py' and create a class in that file
Create another python file 'ObjectInAnotherFile.py' and create object for the class and run the file.

ClassInOneFile.py - In this file a class is created with a constructor and a function. Sum of the two numbers are doing in constructor. Multiplication is doing inside function and it returns the result

```python
class Example:
    def __init__(self,a,b):
        print("this is constructor")
        c=a+b
        print("the sum is: " + str(c))

    def functionMultiply(self,a,b):
        print("this is a function")
        c=a*b
        return c
```

ObjectInAnotherFile.py - In this file, import the file where the class is already written.
While creating the object of the class syntax is

```python
obj=filename.classname()
```
 Object of the class is created. Constructor with arguments are called, when the object is defined. Function to multiply is called

```python
import ClassInOneFile

obj=ClassInOneFile.Example(10,20)
x=obj.functionMultiply(10,20)
print("The multiplication is: " + str(x))
```

Program output : (on running ObjectInAnotherFile.py)

```powershell
this is constructor
the sum is: 30
this is a function
The multiplication is: 200
```
## Modules
1. Modules can be defined as python files(with .py extension), it can have executable code, module functions and class
2. Classes also can have functions,properties(Variables) and constructors
Whatever file we create inside python project with .py extension is called python module

### How python module works
* Create a file under python project. Give any name say PyModule.py
* Write any executable code on the file
* Write a function. This is called module function.Functions inside python file, but not inside class are called module functions
* Write a class, write a constructor and function inside the class

PyModule.py
```python
#This is python module
#Here we are writing executable code
print("This is an executable code in python module")

#Here is a module function to find of two numbers
def ModuleFunction(a,b):
    c=a+b
    print("the sum of two numbers inside module function: "+ str(c))

#Here is class
class ModuleClass:
    #Here is a constructor
    def __init__(self):
        print("this is a constructor")
    #Here is a class function
    def ClassFunction(self):
        print("this is a class function")
```
Program output:
When you run PyModule.py, only the executable code runs.

```powershell
:\Work\MyProject\venv\Scripts\python.exe C:/Work/MyProject/PyModule.py
This is an executable code in python module
```
* Now create another file, say AutomationStart.py to use the module file PyModule.py
* First import the module file PyModule.py using the import function
* When you run AutomationStart.py now, the executable code written in PyModule.py runs
*  Now call the module function defined on PyModule.py with syntax
   Modulefile.modulefunction()
* When you call the module function, it runs on 'AutomationStart.py'
* Now create the object of the class to call the function. once the object of the class is created constructor calls automatically. To create the object the syntax is
  obj=Modulefile.classname

AutomationStart.py

```python
#Import the module
#whenever we are importing any module, that module executable code will run
import PyModule

#Whenever you call any module function it runs
PyModule.ModuleFunction(10,20)

#To use any function inside the class,create object of the class and call the function using object
obj=PyModule.ModuleClass() #Constructor executes when the object of the class is created
obj.ClassFunction()
```

Program output:

```powershell
This is an executable code in python module
the sum of two numbers inside module function: 30
this is a constructor
this is a class function
```
### Create project structure
To create a project structure we need to maintain a tree
with modules
with directories
classes and executable code
* Create a project in PyCharm, say TestAutomation
* Inside project you can create n number of directories say Library, Pages, TestCases, Utility etc
* Inside directories you can create n number of modules with .py extension
  Example
  Project : TestAutomation
  Directories : Library, Pages, TestCases, Utility
  Library : create a module CommonModule.py and write some common codes here
  Utility : Create a module Screenshot.py and write the code to take the screenshot
  Pages : Inside pages create another directory Login, inside login create a module LoginWithuserName.py and write the code for that

## Difference between import and from-import
We need to use python files created in one directory/modules to another.
There are two methods to import module files
1. use import statement
2. use from module import class
   
import method - this imports all the classes in the module file.
                While creating the object of the class, need to give the entire directory structure
                syntax :
                import directory structure
from import method - imports only specified classes in the module file
                    while creating the object of the class, directory structure is not needed
                    from directory structure import class name

Example to demonstrate the difference of import and from import method
The project structure
Project name : TestAutomation
Directories/Module 
1. Library/CommonModule.py
2. Pages/Login/ABC.py
3. TestCases/Tcase.py
4. Utility/Snapshot.py

In CommonModule.py, two classes are created and this is been used in Tcase.py

CommonModule.py

```python
class A:
    def __init__(self):
        print("This is A class constructor")
    def startBrowserA(self):
        print("A class method")
        print("Starting browser")

class B:
    def __init__(self):
        print("this is B class constructor")
    def startBrowserB(self):
        print("B class method")
        print("Starting browser")
```
on Tcase.py, the CommonModule.py has to be imported

TCase.py

import method
```python
import Library.CommonModule
#Create object of class A
objA=Library.CommonModule.A()
objA.startBrowserA()

#Create object of class B
objB=Library.CommonModule.B()
objB.startBrowserB()
```
Here while using the import method, all classes inside the module gets imported.And while creating the object the full directory structure has to mention

from import method

```python
from Library.CommonModule import A,B  #You can specifically mention the class names you want to import
objA=A()
objA.startBrowserA()

objB=B()
objB.startBrowserB()
```
Here in from import method, class names to be imported can be specifically mention.Also while creating the object the full directory structure is not needed.

## File Handling
1. We can create an object of File class by calling pre defined Open method
2. We need to open file by setting opening mode
   r - read mode
   w - write mode
   a - append mode
   r+ - read and write mode
   w+ - write and read mode
   a+ - append and read mode

### Read data from the file
*  Create a txt file in your system and write something in it
*  Open Pycharm and create a file say 'FileRead.py'
*  First open the file using open method. You need to give the txt file path
*  mode r, is used for read mode
*  read method  is used to read data from the file

FileRead.py
### To read all data from the file
read method is used

```python
#To open the file
obj=open("C:\Work\PyFile.txt",'r')
#Read method can read all data from the file
print(obj.read())
```

Program ouput:

```powershell
This is python file
This is line 1.
This is line 2.
This is line 3.
```
### To read only one line from the file
readline method is used. it reads only one line at a time. If you want to read n lines write the readline code n times

```python
obj=open("C:\Work\PyFile.txt",'r')
#Read only one line from the file.
print(obj.readline()) #readline method reads the first line
print(obj.readline()) #reads second line
```
Program output:

```powershell
This is python file

This is line 1.
```
### Read only a few characters in the file
We can limit the read method by giving the no of characters to read

```python
obj=open("C:\Work\PyFile.txt",'r')
#Read only few characters in the file
print(obj.read(10)) # it reads the first 10 characters
```
Program output:

```powershell
This is py

```

### Read character by character and line by line
#### Read all characters from the line and display one by one

```python
obj=open("C:\Work\PyFile.txt",'r')
#Read all characters from the line and display one by one

for i in obj.read():
    print(i)

```
Program output:

```powershell
T
h
i
s
 
i
s
 
p
y
t
h
o
n
 
f
i
l
e
```
#### Read all data from file line by line

```python
#read all data from file line by line
obj=open("C:\Work\PyFile.txt",'r')
s=obj.readline() #first line is stored to s
while(s): # if s exits, the s is printed
    print(s)
    s=obj.readline() # now second line is stored to s
```

Program output:

```powershell
This is python file

This is line 1.

This is line 2.

This is line 3.
```
### Write data to the file(.txt   )
Use the function open("filename","w+") to create a file. The + tells the python compiler to create a file if it does not exist.
You can write also by using this function.

Program to create a file and write 10 lines to it.

```python
file1=open("C:\Work\MyFile.txt","w+")
#write 1 to 10 lines
for i in range(10):
    file1.write("this is line" + str(i+1) + "\r\n" )
file1.close()

#prints the file in console
file1=open("C:\Work\MyFile.txt","r")
print(file1.read())
```
Once the program is run, check in your system whether the file with name MyFile.txt is created and 10 lines are wrote in to it

Program output:

```powershell
this is line1

this is line2

this is line3

this is line4

this is line5

this is line6

this is line7

this is line8

this is line9

this is line10
```
### Append data to the file
To append data to an existing file use the command open("Filename", "a"). If the file does not exist, it creates a new file.
Append to the above file 2 more lines

```python
#Open the file in append mode
file1=open("C:\Work\MyFile.txt","a+")

#append two more lines to the above file
for i in range(2):
    file1.write("Append line " + str(i+1) + "\r\n")

#To read and print the file data in console
file1=open("C:\Work\MyFile.txt","r")
print(file1.read())
```

Program output:

```powershell
this is line1

this is line2

this is line3

this is line4

this is line5

this is line6

this is line7

this is line8

this is line9

this is line10


this is line1

this is line2

this is line3

this is line4

this is line5

this is line6

this is line7

this is line8

this is line9

this is line10

Append line 1

Append line 2
```

### File methods tell() and seek()
Tell method tell the current cursor position in the file
Seek method is to navigate the cursor to different position in the file

```python
#First read a file
obj=open("C:\Work\PyFile.txt",'r')
print(obj.tell()) #cursor position is 0
obj.readline()
print(obj.tell()) #now cursor position is 21
#Seek method to navigate your cursor to different position
obj.seek(60)
print(obj.tell()) # cursor position is 60
```

Program output:

```powershell
0
21
60
```
## Exception handling in python
* While creating any code if we get error in runtime, this type of error is called runtime error or logical error or exception
  Task which we need to perform in case when we get exception is called exception handling.

The below program to get the sum of two numbers, throws an exception if user tries to give any non-integer value.

```python
userNum1=input("Please enter first number -->")
userNum2=input("Please enter second number -->")
result=int(userNum1)+int(userNum2)
print("The sum is: " + str(result))
```

Program output:

```powershell
Please enter first number -->45d
Please enter second number -->rts
Traceback (most recent call last):
  File "C:/Work/TestAutomation/Utility/TellAndSeek.py", line 14, in <module>
    result = int(userNum1) + int(userNum2)
ValueError: invalid literal for int() with base 10: '45d'
```
In the above case,when any exception comes, we need to handle it by using exception handling.

### Handling exception using try, exception and finally
Exception handling can be done by using
try: whatever code is expected to throw an exception is put inside try
except: whatever code to perform in case of exception
finally: whatever code you want to execute at the end

```python
try:
    userNum1=input("Please enter first number -->")
    userNum2=input("Please enter second number -->")
    result=int(userNum1)+int(userNum2)
    print("The sum is: " + str(result))
except:
    print("your input is incorrect, please enter correct numbers")
finally:
    print("This code to execute at the end")
```
Program output when you give valid input data:

```powershell
Please enter first number -->30
Please enter second number -->50
The sum is: 80
This code to execute at the end
```
Program output when you give any invalid data:

```powershell
Please enter first number -->30sdd
Please enter second number -->67vv
your input is incorrect, please enter correct numbers
This code to execute at the end
```
## Read data from configuration file
Why we want to read data from configuration file?
1. Lot of data which are configurable can be placed from config file
2. It will be easy to change that data
Suppose in automation, some 100 test cases uses username and password. When username and password changes we need to change that in 100 files. In this case, we write such kind of code in configuration file. Thus we can change the data in config file only, rather than changes in all places.

### How to create config file
* On pycharm,create a new file and the extension should be .cfg
* On config file, we need to create sections 
```python
[Section1]
```
* Inside section give any number of variables
```python
[Section1]
Variable1
Variable 2
```
### Read data from config file
* Import config parser class from config parser
* Create object of config parser class
* Read data from the config file using read method
* Get data from the config file using get method by passing two arguments- Section and Variable
  
Create Config.cfg inside project/directory, as an example TestAutomation/InputFiles/Config.cfg
Create another file under project ReadDataFromConfig.py and use Config.cfg here

Config.cfg

```python
[Section1]
username=testing
password=automation
```
ReadDataFromConfig.py

```python
#import configparser class from configparser
from configparser import ConfigParser

#Create object of config parser class
configObj=ConfigParser()

#To read data from the config file
#Need to give path of the config file. rightclick on config.cfg file and get the path. The path should have forward slashes /
#configObj.read("C:/Work/TestAutomation/Config.cfg")
#Here we are taking the path of the config file. This might change and if you want to share the code to others.
#For that create a directory and put the config file over there. Say the directory name is InputFiles. Put Config.cfg inside InputFiles

configObj.read("./InputFiles/Config.cfg")

#Now get data from the config file. Give section name and the variable
print(configObj.get("Section1","username"))
```
Program output:

```powershell
testing
```

## OOPS Programming
### Inheritance
* With the help of inheritance we can transfer properties of a class to another class
* Class which is inherited is called Parent class, class with inherit another class is Child class
* After inheritance, child class gets its own item as well as parent class items
* While creating the childclass, we need to specify inheritance by the below syntax
  ```python
  class ChildClass(ParentClass)
  ```
* Inheritance are of different types - Single inheritance, Multilevel inheritance, Multiple inheritance

Inheritance program

1. Create a file 'Inheritance1.py' and write a parent class and parent method
   
```python
   class ParentClass:
    def ParentClassMethod(self):
        print("this is parent class method")
```
2. Create a file 'Inheritance2.py' and write a child class and child class method
   
```python
 #import the parent class
 from Inhertitance1 import ParentClass

#Inhertiance is calling in child class with argument as parent class
class ChildClass(ParentClass):
    def ChildClassMethod(self):
        print("this is child class method")
```
3. Create a file 'Inheritance3.py' and create object of the child class and call child method as well as parent method

```python
from Inhertitance2 import ChildClass
#Need to create object of child class only. By using child class object parent class object can also be called
obj=ChildClass()
obj.ChildClassMethod()
obj.ParentClassMethod()
```
Run 'Inheritance3.py' file and on output you can see both the childclass method and parent class method is called

Program output:

```powershell
this is child class method
this is parent class method
```

### Importance of Inheritance
Its reduces the duplicate codes as well as reusability.
When child class inherits parent class, need to create object of the child class only. By that object parent class methods can also be called.
The below program explains inheritance

### Single inheritance
When one parent class and one child class, it is single inheritance

Suppose two developers in a team.
Dev1 needs to create methods for sum and subration 
Dev2 needs to create sum,subtraction and multiply 
If Dev2 creats sum and sub again,that leads to duplicate codes. So Dev1 can create a class with two methods sum and sub, and Dev2 can use both of them in her class. Here Class A act as parent class and Class B act as child class.

Dev1 - Creates A.py with ClassA and methods for sum and sub
Dev2 - Creates B.py with ClassB with method for multiplication. ClassB inherits class A . And thus sum and sub method can be inherited.Here ClassA is parent and ClassB is child class.
Creates another file c.py and create object of child class and call the methods for sum,sub and multiply

A.py
```python
class classA:
    def sum(self,a,b):
        c=a+b
        print("The sum of two numbers: " + str(c))
    def sub(self,a,b):
        c=a-b
        print("The sub of two numbers: " + str(c))
```
B.py
```python
from A import classA

class classB(classA):
    def multiply(self,a,b):
        c=a*b
        print("The multiplication of two numbers: " + str(c))
```
C.py
from B import classB

obj=classB()
obj.sum(50,60)
obj.sub(70,20)
obj.multiply(80,10)

Run C.py
program output:
```powershell
The sum of two numbers: 110
The sub of two numbers: 50
The multiplication of two numbers: 800
```
### Multiplevel inheritance
When a class is derived from a class which is also derived from another class, i.e. a class having more than one parent classes, such inheritance is called Multilevel Inheritance. The level of inheritance can be extended to any number of level depending upon the relation. Multilevel inheritance is similar to relation between grandfather, father and child. 

Class A -> Class B -> Class C etc . Here Class A is parent class for Class B. Class B is the parent class for Class C. ClassA is the super class. 

Since Class B inherits Class A methods and Class C inherits both Class A and B methods, need to create object of Class c only. using that object, Class A ,B and C methods can be called

File1.py
```python
class A:
    def AClassMethod(self):
        print("this is class A method")

class B(A):
    def BClassMethod(self):
        print("this is class B method")

class C(B):
    def CClassMethod(self):
        print("this is class C method")
```

File2.py
```python
from File1 import C

obj=C()
obj.AClassMethod()
obj.BClassMethod()
obj.CClassMethod()
```
Program output:

```powershell
this is class A method
this is class B method
this is class C method
```
##Multiple inheritance
Class have more than one parent class. And when a child class inherits multiple parent class, it is called multiple inheritance.
Class A (parent class)- Method1 and Method2
Class B (parent class)- Method3 and Method4
Class C (Child class) - Inherits Method1,Method2,Method3 and Method4. Also it can have its own methods, say Method5 or so

MultipleInheritance1.py

```python
class A:
    def AClassMethod(self):
        print("this is class A method")

class B:
    def BClassMethod(self):
        print("this is class B method")

#Class C inherits both A and B
class C(A,B):
    def CClassMethod(self):
        print("this is class C method")
```

MultipleInheritance2.py
```python
from MultipleInheritance1 import C
#Since class C inherits both class A and B, need to create the object of Class C only
obj=C()
obj.AClassMethod()
obj.BClassMethod()
obj.CClassMethod()
```
Run MultipleInheritance2.py file

Program output:
```powershell
this is class A method
this is class B method
this is class C method
```
### Constructors in inheritance
Constructors in both parent and child class
In java and C++, when you create object of the child class, the parent class constructor also call automatically.
But in python the logic is bit different. 
1. If parent class has constructor and if child class has no constructor, on creating the object of the child class, it first checks if child class has constructor. If not the parent class constructor is called
2. If parent class and child class both has constructors, on creating the object of the child class, it calls only the child class constructor. If you want to call the parent class constructor, the object of the parent class has to be created.



In this program Class A is parent class and Class B is child class. We defined constructor on parent class only
Inheritance1.py

```python
class classA:
    def __init__(self):
        print("this is parent class constructor")
    def sum(self,a,b):
        c=a+b
        print("The sum of two numbers: " + str(c))
    def sub(self,a,b):
        c=a-b
        print("The sub of two numbers: " + str(c))
#Class B inherits class A
class classB(classA):
    def multiply(self,a,b):
        c=a*b
        print("The multiplication of two numbers: " + str(c))
```

inheritance2.py

```python
from Inheritance1 import classB

obj=classB() # constructor is called. It first checks for child constructor. If child constructor not present calls the parent constructor
obj.sum(50,60)
obj.sub(70,20)
obj.multiply(80,10)
```

program output:

```powershell
this is parent class constructor
The sum of two numbers: 110
The sub of two numbers: 50
The multiplication of two numbers: 800
```

In this program Class A is parent class and Class B is child class. We defined constructor on both parent and child classes
Inheritance1.py

```python
class classA:
    def __init__(self):
        print("this is parent class constructor")
    def sum(self,a,b):
        c=a+b
        print("The sum of two numbers: " + str(c))
    def sub(self,a,b):
        c=a-b
        print("The sub of two numbers: " + str(c))
#Class B inherits class A
class classB(classA):
     def __init__(self):
        print("this is child class constructor")
    def multiply(self,a,b):
        c=a*b
        print("The multiplication of two numbers: " + str(c))
```

inheritance2.py

```python
from Inheritance1 import classB

obj=classB() #constructor is called. It first checks for child constructor. If child constructor is present it calls the child constructor. Parent constructor is not called
obj.sum(50,60)
obj.sub(70,20)
obj.multiply(80,10)
```

program output:

```powershell
this is child class constructor
The sum of two numbers: 110
The sub of two numbers: 50
The multiplication of two numbers: 800
```
To get the constructor of both parent and child class

inheritance2.py

```python
from Inheritance1 import classB,classA

obj=classA() ##to call the constructor of parent class
obj=classB() #constructor is called. It first checks for child constructor. If child constructor is present it calls the child constructor. Parent constructor is not called
obj.sum(50,60)
obj.sub(70,20)
obj.multiply(80,10)
```
program output:

```powershell
this is parent class constructor
this is child class constructor
The sum of two numbers: 110
The sub of two numbers: 50
The multiplication of two numbers: 800
```
### Data overriding
If the parent and child class have same name and same signature method is called overriding.
The method which is written in parent class can be used in child class with same name and signature,but logic can differ
Method overriding works only with inheritance. This is a best example for inheritance

Why method overriding is needed?
Suppose in a team Mem1,Mem2,Mem3 writing a piece of code
Mem1 - ClassA - to write methods for sum and sub
Mem2 - ClassB - to write methods for add, sub and mul. Here she inherits sum and sub methods from the parent class(ClassA)
Mem3 - She is going to call these methods in her piece of code. Object of childclass(ClassB) is created. Called the functions sum, sub and Mul. But Mem3 wants to change the logic of 'sub' method and she asks for that to Mem2. Mem2 has not created sub method as her own.She has just inherited that from Mem1. So in this case Mem2 writes her own sub method in child class(ClassB), with same function name and signature as in parent class. And changes the logic inside function body. Hence Mem2 is overwriting a same method in child class, without changing it in parent class.
Now when Mem3 calls the sub method by child class object, the method inside child class gets executed.

Program to explain overriding
File1.py

```python
class A:
    def sum(self,a,b):
        print(a+b)
    def sub(self,a,b):
        print(a-b
```

 File2.py
```python
 from File1 import A

class B(A):
    #Method overriding. Using the parent class method sub here with different logic
    def sub(self,a,b):
        print(b-a) #Logic of the sub is changed

    def mul(self,a,b):
        print(a*b)
```

File3.py

```python
from File2 import B

obj=B()
obj.sum(10,20) #from parent class
obj.mul(10,20) #from child class
obj.sub(20,10) #from parent class. Now we need to change the logic to (b-a), method can be overwrite in child class with same name and signature
```

Run File3.py

Program output:
```powershell
30
200
-10
```
## Read data from excel sheets
### Why read data from excel sheets?
When we want to execute testcase with multiple type of test case,mostly we place the data in excel sheet.Only one automation test case we write that executes multiple test data from excel sheet
Example:
step of the test case is same, but test data is different.
To login to a site. The test case is same, but we can try using different test data like valid data, invalid data, with capitals etc

### Which library we need to pick data from the excel?
library xlrd is used for picking data from the excel.
### How to set up the library for excel
* start command prompt
* type the command pip install xlrd
* when you enter the command, it picks all the files related to xlrd and download the files

### Read data from excel using XLRD module
1. import xlrd module
2. create workbook object
3. create worksheet object
4. create cell object

1. program to print number of sheets on the excel
```python
import xlrd
#We need to create the object of the workbook
wk=xlrd.open_workbook("C:/Work/testdata.xls")

#nsheets method prints number of sheets on the excel sheet
print(wk.nsheets)
```

you will get an error while running th  above code
ModuleNotFoundError: No module named 'xlrd'

for fixing this we need to install xlrd on pycharm
pycharm -> file -> settings -> project:[project name] -> project interpreter -> intall xlrd package
Run the program again it prints the number of sheets in the excel workbook

2. Program to explain how to create object of the workbook, work sheet and cell of the excel. Also it explains how to find number of sheets in a workbook. How to find number of rows and columns in a sheet. How to find the cell value

pre-requistic :Create an xls sheet in your system. Create n number of sheets you want. Enter values to rows and columns in any sheet
```python
import xlrd
#We need to create the object of the workbook
wk=xlrd.open_workbook("C:/Work/testdata.xls") #specify the path of xls sheet 

#nsheets method prints number of sheets on the excel sheet
print(wk.nsheets)

#Now we want to move to sheet level. We can find sheet by index or sheet name
#Finding sheet by using the index
#create object of sheet
ws=wk.sheet_by_index(1)

#to find number of rows on the sheet
print(ws.nrows)

#to find number of columns on the sheet
print(ws.ncols)

#finding the sheet by sheet name
ws=wk.sheet_by_name("Sheet1")
#to find number of rows on the sheet
print(ws.nrows)

#to find number of columns on the sheet
print(ws.ncols)

#Now we want to move to cell
#Need to create the object of the cell
wc=ws.cell(0,0) #first row first column
print(wc.value)
wc=ws.cell(0,1) #first row second column
print(wc.value)
wc=ws.cell(1,0) #second row first column
print(wc.value)
wc=ws.cell(1,1) #second row second column
print(wc.value)

#suppose i placed a data in row 15 and col 1
wc=ws.cell(14,0)
print(wc.value)
#suppose i placed a data in row 15 and col 7
wc=ws.cell(14,6)
print(wc.value)
```
Program output:
```
3
15
7
15
7
data1
data11
data2
data22
row15Col1
Row15col6
```
### Read data from all rows and all columns
Program to read all data from excel, from all rows and columns. We need to create the object of workbook and sheet. Once sheet object is created, need to find the number of rows and number of columns.
Use for loop, and final range for reading column value should be the no of columns and the final range to read row value is the no of rows.
create the object of the cell, by passing the values from the loop. finally print the values using the cell object

```python
import xlrd
#object of workbook
wk=xlrd.open_workbook("C:/Work/testdata.xls")
#object of sheet
ws=wk.sheet_by_name("Sheet1")
#number of rows
rn=ws.nrows
#number of columns
cn=ws.ncols

#To read all data from rows and columns in excel
#Going to run a loop for number of rows
for i in range(0,rn): #indexing start from 0, so initial range 0 and final range no of rows
    for j in range(0,cn):# for reading all the columns. initial range 0 and final range no of columns
        wc=ws.cell(i,j)  #object of the cell.
        print(wc.value)
```
Program output:

```powershell
data1
data11
data2
data22
data3
data33
```
Note : xlrd package can be used o-in xls as well as xlsx file as well
Only difference is give the xlsx extension while creating the object of the workbook.
```python
import xlrd
#object of workbook
wk=xlrd.open_workbook("C:/Work/testdata.xlsx")
```

### Writing data to the Excel sheet
To write data to the Excel sheet in XLS format we need XLWT module
To write data to the Excel sheet in XLSX format we need XLSXWRITER module

#### Write data to excel sheet in XLS format
xlwt library is used 
#### How to set up the library for excel
* start command prompt
* type the command pip install xlwt
* when you enter the command, it picks all the files related to xlwt and download the files

Go to pycharm and install xlwt package
pycharm -> file -> settings -> project:[project name] -> project interpreter -> intall xlwt package

Create a python file and import xlwt

```python
import xlwt
#First we need to create the workbook.
wk=xlwt.Workbook()

#To create object of the worksheet, with sheet name
ws=wk.add_sheet("Testing")

ws.write(0,0,"data1")
ws.write(0,1,"data2")
ws.write(1,0,"data3")
ws.write(1,1,"data4")

#Save workbook in the system
wk.save("C:/Work/testingworld.xls")
```
Program Output:
The workbook named 'testingworld' in xls formatis created in your system in the specified location

#### Write data to excel sheet in XLSX format
xlsxwriter library is used 
#### How to set up the library for excel
* start command prompt
* type the command pip install xlsxwriter
* when you enter the command, it picks all the files related to xlwt and download the files

Go to pycharm and install xlsxwriter package
pycharm -> file -> settings -> project:[project name] -> project interpreter -> intall xlsxwriter package

Create a python file and import xlsxwriter

```python
import xlsxwriter

wk=xlsxwriter.Workbook("C:/work/testing.xlsx")
worksheet=wk.add_worksheet("testing1")
worksheet.write('A1', 'Hello')
worksheet.write('B1', 'Good')
worksheet.write('C1', 'Morning')
worksheet.write('D1', 'GoodDay')
wk.close()

```
Program Output:
The workbook named 'testing' in xlsx format is created in your system in the specified location

## Read and write Excel data(XLSX file): OpenPyXl package
OpenPyXl package is a new package that works with XLS and XLSX formats
### How to set up the OpenPyXl library for excel
* start command prompt
* type the command pip install OpenPyXl
* when you enter the command, it picks all the files related to xlwt and download the files

Go to pycharm and install OpenPyXl package
pycharm -> file -> settings -> project:[project name] -> project interpreter -> intall OpenPyXl package

Create a python file and import OpenPyXl

The below program shows how to
* load a workbook using load function
* print the sheetnames
* to create the object of which sheet you want to work on
* Methods to fetch data from the cell
  
 ```python
  import openpyxl

#To load workbook
#Load function
workbook=openpyxl.load_workbook("C:/Work/TestDataXLSX.xlsx")

#to print the sheetnames in the workbook
print(workbook.sheetnames)

#to print which is the active sheet. The sheet which is by default open is active sheet
print(workbook.active.title)

#which sheet you want to work on. Create object of that sheet
sheet=workbook['testing1']
print(sheet.title)

#Methods to fetch data from the cell
print(sheet["A2"].value) #this prints the data in the specified cell

#fetch by creating the object of the cell.
cell1=sheet.cell(1,1) #first row and first column
print(cell1.value)

cell1=sheet.cell(1,2) #first row and second column
print(cell1.value)

cell1=sheet.cell(2,1) #second row and first column
print(cell1.value)

cell1=sheet.cell(2,2) #second row and second column
print(cell1.value)

#Fetch method using keyword arguments
cell1=sheet.cell(column=1,row=3)
print(cell1.value)

cell1=sheet.cell(row=2,column=3)
print(cell1.value)

#This shows for which row and column the last object is shown
print(cell1.row)
print(cell1.column)
```

### To read data from all cells and rows
First method using for loop 

```python
import openpyxl
#To load workbook
workbook=openpyxl.load_workbook("C:/Work/TestDataXLSX.xlsx")
sheet=workbook["testing1"]
#How many rows having data
r=sheet.max_row
#How many columns having data
c=sheet.max_column

print("the no of rows: " +str(r))
print("the no of rows: " +str(c))

for i in range(1,r+1): #final range skips the last value. so you need to give as rows+1
    for j in range(1,c+1):#final range skips the last value. so you need to give as columns+1
        wc=sheet.cell(i,j)
        print(wc.value)
  ```
Second method using for loop inside cell range

```python
import openpyxl
#To load workbook
workbook=openpyxl.load_workbook("C:/Work/TestDataXLSX.xlsx")
sheet=workbook["testing1"]
#How many rows having data
r=sheet.max_row
#How many columns having data
c=sheet.max_column

print("the no of rows: " +str(r))
print("the no of rows: " +str(c))

# first move through each row in the range where data is enteres
#then move through each column in the row and print the column value
for row in sheet['A1':'D3']:
    for col in row:
        print(col.value)
```

### Write data to the excel sheet :OpenPyXl package

* first import the OpenPyXl package to the python file
* Create the object of the workbook
Once you create the object of the workbook, the workbook has created internally.Once you save only it saves on the desired location
* By default we have a sheet over there. If only one sheet that is the active sheet.
* create object for the active sheet and give a title for that sheet
* To put any data on the sheet,pass the cell index and value
* Create sheet function is used to create more sheets
* Enter data in to second sheet
* We can remove sheet by remove function
  
This program creates an excel sheet with xlsx format in the location specified.
This created two sheets and write something to the cells in the sheet.

```python
import openpyxl

#Create workbook object.
workbook=openpyxl.Workbook()

#get the active sheet
sheet=workbook.active
#By deafukt one sheet will be present in the workbook and that sheet is the active one
#give a title to the sheet
sheet.title="testing1"
#Add value to any cell
sheet['A1'].value="hello"
sheet['A2'].value="world"

#To create another sheet
workbook.create_sheet(title="testing2")
#To create object of second sheet
sheet2=workbook['testing2']
sheet2['A2']="goodday"

#Saving the sheet
workbook.save("C:/work/Pysheet.xlsx")
```
## Working with CSV file
CSV files are comma seperated files. We can see how to
* Read content from CSV file
* Read all content from CSV through looping
* Write content to CSV file

### Read content from csv file
1. First Create a csv file in your system. For that open Notepad++, enter some records like emp id, employee job, age. Save this file in your system
2. Create a python file on pycharm
3. import csv module to work with csv files. For that no need to install the package of the csv. By default it will be present on the pycharm
4. Open the csv file, using file handling open method. Give the path of the file
5. To render the file in the form of csv, csv module has a method  'reader'. Call the reader method and pass the object of the file
6. This rendered file can be converted to list and can read the data from the list
7. Print the list. It prints the data in the form of list inside list

```python
import csv
#open the file
file1=open("C://work/TestData.csv")
#reader method to render the file in the form of csv
csv_data=csv.reader(file1)
#convert the csv file to list
list1=list(csv_data)
#print the list
print(list1)
```
Program output:

```powershell
[['id', 'emp', 'age'], ['John', 'tester', '30'], ['Sara', 'technical writer', '32'], ['Anna', 'manager', '40'], ['Elsa', 'developer', '25']]
```
### Read all content from csv through looping
First approach
1. Go to each element in the list. The above program gives an output in list with 5 rows. Each row itself is a list
2. Run a loop, to iter to each row in the list
3. Find the length of each row, print the elements in the row.

```python
import csv
#open the file
file1=open("C://work/TestData.csv")
#reader method to render the file in the form of csv
csv_data=csv.reader(file1)
#convert the csv file to list
list1=list(csv_data)
#print the list
print(list1)

#list will be printed with data in rows. Each row is again a list itself.
#to print each element of the list, iter to each row, till the length and print all elements in the list.
for row in list1:
    lrow=len(row)
    for element in range(0,lrow):
        print(row[element])
```

Program output:

```powershell
id
emp
age
John
tester
30
Sara
technical writer
32
Anna
manager
40
Elsa
developer
25
```
Second approach

1. Find the length of the list. the length of the list in the above program is 5
2. run a loop, to iter through each element of the list till its length. 
3. print each element in the row

```python
port csv
#open the file
file1=open("C://work/TestData.csv")
#reader method to render the file in the form of csv
csv_data=csv.reader(file1)
#convert the csv file to list
list1=list(csv_data)
#print the list
print(list1)
#length of the list
lenlist=len(list1)

#for loop to iter till the length of the list and print each element in the row
for i in range(0,lenlist):
    print(list1[i][0])
    print(list1[i][1])
    print(list1[i][2])
```
Program output:

```powershell
id
emp
age
John
tester
30
Sara
technical writer
32
Anna
manager
40
Elsa
developer
25
```
### Write data to CSV file

1. Open a new python file in pycharm
2. import csv module
3. to create a new file in the system , we need to open a csv file in write mode. speciy the path and newline, to print data in new line in csv
4. call csv writer method, to write the data to csv
5. to write use the method writerow method and write the data in the form of the list 

```python
import csv
#Open file in write mode
file1=open("C://work/Newfile.csv",'w',newline='')
csvWrite=csv.writer(file1)

#csvWrite.writerow(['emp','id','age'],['abc','123','20'],['efg','1234','30']) - this is wrong. writerow takes exactly one argument

csvWrite.writerow(['emp','id','age'])
csvWrite.writerow(['abc','id-123','30'])
csvWrite.writerow(['def','id-15543','40'])

file1.close()
```

Program output: 
A csv file with name Newfile.csv is created in the specified path "C://work/" with the data entered in each row.

## Compare Data - Assert in python
* Using assert we can compare actual result with the expected result
* Assert is by default available in python
* When we are comparing data, if it is failed we can display a failure message
* Assert statement simply takes input a boolean condition, if the condition is true it does no return anything, but if it is  false, then it raises an AssertionError along with the optional message provided.
* If we use assertion in a method, if the condition checks fails the remaining code of that method is not executed. It will continue with the next test method.

### Syntax of assertion
Syntax : assert condition, error_message(optional)

Parameters :
condition : The boolean condition returning true or false.
error_message : The optional argument to be printed in console in case of AssertionError

Returns :
Returns AssertionError, in case the condition evaluates to false along with the error message which when provided.

  
### Program to demostrate assert statment
Takes a user number and if the number is greater than 100, print data is incorrect.

```python
#Take a user number

userNum=input("Enter the number -->")
userNum=int(userNum)

assert userNum<100, ["the data is incorrect.hence execution failed"]
print("the remaining code is executed")
```

Program output:
If you give a number less than 100

```powershell
Enter the number -->25
the remaining code is executed
```

If you give a number greater than 100

```powershell
Enter the number -->125
Traceback (most recent call last):
  File "C:/Work/OOPS/Assertion.py", line 6, in <module>
    assert userNum<100, ["the data is incorrect.hence execution failed"]
AssertionError: ['the data is incorrect.hence execution failed']
```
## Project 1 : Webscraping using Python
### What is Webscraping?
Web scraping(also defined as Web data extraction or Web harvesting) is a technique to extract large amounts of data from website whereby the data is extracted and saved to a local file in your computer or to a database in table(spreadsheet) format.
On daily basis we are going to different websites and reading data over there. Sometimes we need to save the data so that we can use it when we are offline.Also many companies use webscraping to save the reviews of the product so that they can analyse it later on to make decisions. Webscraping is also used to fetch data from different websites when you are going for a research
### What is the use case of webscraping?
When we go to google and type something. Example we need to search testing. google displays many websites related to software testing.How google knows the websites are related to testing?  whenever a website is launched and registered with google, google continuosly going through the data of the website and scraping the contents. Whenever you are typing some keyword, google can easily identify the keywords and display the results. 

### Webscraping using python
#### Install modules required for webscraping
Two modules of python are required
1. requests module - to make requests to any webpage
2. bs4 module(BeautifulSoup) - this module is required for parsing the html files

To install the above libraries
* Go to command prompt
* type the command - pip install requests
* wait till the package download is completed
* now type the command - pip install bs4

Go to pycharm and install requests and bs4 package
pycharm -> file -> settings -> project:[project name] -> project interpreter -> install requests and bs4package
#### Pick data and display on console
Requests module is used to make requests to the webpage.
* Create a new project in pycharm
* Create a python file inside the project
* import the requests module
* to fetch data from website, first we need to send request with the URL
* Whatever response we get from the URL, save it in an object 'response'
* print the response text. Here we get the complete html data of the web page
* you can check the status code of the response as well
  
Program to pick data and display the html data on the console

```python
#import the requests module
import requests
#request module to make any request to the website
#Sending request with url
#Fetch data and display on the console
URL='http://www.thetestingworld.com/'
response = requests.get(URL) #whatever response we get from the URL, saving in the object 'response'
print(response.text) # we are getting html of that page. complete html of any page
#Check status code
#printing status code 200
print(response.status_code)
```

Program output:
It print the complete html of the webpage

#### pick data and save it in a file
On previous section, we have seen how to display html data on the console.
Here we can see, how we can save the html data in a file to your system
* import the requests module
* fetch data by passing the URL
* store the response from the page in to an object 'response'
* open a file in write and binary mode.We have to maintain the unicode of the data hence using the binary mode
* write a for loop to fetch the response data and save it to the file
* iter to each content of the html data and picks 10000 bytes everytime and save in the file

Program to pick data from the console and to save it in a file
```python
import requests
#request module to make any request to the website
#Sending request with url
URL='http://www.thetestingworld.com/'
response = requests.get(URL) #whatever response we get from the URL, saving in the object 'response'
#open a file in write and binary mode. We have to maintain the unicode of the data. hence using binary mode
file1=open('C://work/result.txt','wb')

# loop to fetch the response data and store in the file
#iter to the content of the html data. everytime it picks 10000 byes and save in the file
for data in response.iter_content(10000):
    file1.write(data)

file1.close()
```

Program output:
A file with name result.txt saves in the location C://work and it contains the complete html data of the webpage

#### Fetch the data using beautifulSoup
beautifulSoup (bs4) module is used for parsing HTML and XML modules

* import bs4 module in python file
* import the requests module for sending the requests to url
* store the response of the url in the object 'response'
* parse the html response data , to find each elements in the data
* for parsing the html data use beautifulSoup
* save the parsed data to an object
* use CSS locator to get the elements from the parsed data
* first find all the links in the parsed data using the CSS locator 'a'
* find how many links in the page
* using that run a 'for' loop to iterate to each and every element and find text of all the links, URL of all the links, title of all the links and attribute of all the links

Program to explain the above
```python
import requests
import bs4
URL='http://www.thetestingworld.com/'
response = requests.get(URL) #whatever response we get from the URL, saving in the object 'response'
#beautifulSoup (bs4) module is used for parsing HTML and XML modules
#Save the parsed data
parsed_data=bs4.BeautifulSoup(response.text) #Whatever response you get, parse the data using beautifulsoup and save it in parse data
#To get the objects from the parsed data, we can use the CSS locators
#to fetching any data we can use select method
#to select all the links. a is the tag for the links
#all__links are saved in a list
all_links = parsed_data.select('a')
#Here we are using the CSS locator to fetch data. Here we fetched the links. You can use any CSS locator to fetch the data
#how many links. find len of the list
print("how many links on the page")
print(len(all_links))

#We want to go to each of the link and find the text on it
for l in all_links:
    print(l.getText()) #to get the text of all the links.
    #how to print URL of each link
    print(l.get('href')) #href is the tag for url
    #We can fetch value of any attribute like href, title,
    print(l.get('title'))
    #to fetch all the attributes of a particular element
    print(l.attrs)
```
Program ouput:
This program prints 
1. all the links in the webpage
2. total link number
3. text of each link
4. url of each link
5. title of each link
6. attributes of each element

## Get JSON understanding
While testing rest API, we are sending a request. Many cases we need to send body of the request as well.
The body of API could be in JSON format.
* JSON(JavaScript Object Notation) is a lightweight data interchange format. You can send data to the server and vice versa. It is lighweight compared to XML
* JSON is a syntax for storing and exchanging data. Means we can store the data in to it and transfer the data.
* Data is stored in JSON in the form of key value pair. Key should be unique. Each key value pair is seperated by comma. Last key value pair in the JSON does not need a comma.
 ```json
 {
     "Empid": "12344",
     "Name": "Elsa",
     "Age": 23
 }
 ```
 * Value could be in array. If you want to put more than one value in key.
 ```json
 {
     "Empid": "12344",
     "Name": "Elsa",
     "Age": 23,
     "City":["Bangalore","Delhi","Mumbai"]
 }
 ```
 * Value can have further keys and value. We call it as object, if the value has further keys and value. We can have this hierarchy to any level.
 ```json
 {
     "Empid": "12344",
     "Name": "Elsa",
     "Age": 23,
     "City":["Bangalore","Delhi","Mumbai"],
     "Address":
     {
         "HouseNo":"123",
         "StreetName":"ABCD",
         "City":"QWERTY",
         "phonenumber":
         {
             "Mobile":"655575576",
             "LandLine":"767676677"
         }
     }
 }
 ```
### How to write JSON path
JSON path is a path through which we are going to navigate to the different elements uniquely in JSON file.
What is the use of JSON?
If you want to validate any particular data, on the specific place of the reponse we need JSON path.

#### Simple JSON path
Go to 'http://jsonpath.com/', so that you can evaluate your JSON path. If you want to search simple values like 'Name' or 'Age', just give $.Age or $.Name. By this way you cannot evaluate 'Phonenumber' as this is an object inside an object.
#### How to write JSON path in array
In this JSON
 ```json
 {
     "Empid": "12344",
     "Name": "Elsa",
     "Age": 23,
     "City":["Bangalore","Delhi","Mumbai"],
     "Address":
     {
         "HouseNo":"123",
         "StreetName":"ABCD",
         "City":"QWERTY",
         "phonenumber":
         {
             "Mobile":"655575576",
             "LandLine":"767676677"
         }
     }
 }
 ```
 JSON Path to search
 1. city - $.City
   Result:
  [
    "Bangalore",
    "Delhi",
    "Mumbai"
  ]
2. Any city like Delhi - $.City[1] (pass the index of the array)
   Result:
   [
  "Delhi"
    ]
#### How to write JSON path in object
JSON path to search any object inside an object, we can use use dot in between the elements
Path to search
1. StreetName - $.Address.StreetName
   Result:
   [
  "ABCD"
    ]
2. Mobile - $.Address.phonenumber.Mobile
   Result:
   [
  "655575576"
    ]

In the below JSON, find the JSON paths
```JSON
{
  "firstName": "John",
  "lastName" : "doe",
  "age"      : 26,
  "address"  : {
    "streetAddress": "naist street",
    "city"         : "Nara",
    "postalCode"   : "630-0192",
  "phoneNumbers": [
    {
      "type"  : "iPhone",
      "number": "0123-4567-8888"
    },
    {
      "type"  : "home",
      "number": "0123-4567-8910"
    }
  ]
  }
}
```
Find the JSON path of the type home
Since phoneNumbers is an array, we need to pass the index. Since phoneNumbers is an object inside address dot is needed between the objects.
JSON path : $.address.phoneNumbers[1].type


### Working with JSON files
In this section we can see how to
* Parse Dictionary to JSON
* Parse JSON to Dictionary
#### Parse dictionary to JSON
* Open a python file in pycharm and import json module. This module is by default present in python.No need to install the package.
* Create a dictionary in the form of string.
* Using json loads function parse dictionary to JSON format.

```python
#import JSON module
import json

#Create a dictionary in the form of a string
dic='{"k1":"Value1","k2":"Value2"}'

#Parse the dictionary to JSON, by using JSON function loads. Loads function parses the dictionary to json
JSON_result=json.loads(dic)

print(JSON_result) # We get the dictionary in JSON format
```
Program output:

```powershell
{'k1': 'Value1', 'k2': 'Value2'}`
```
### Usecase to show a sample API testing in python
Steps
* send a request to API
* parse response to JSON
* validate by JSON path

This program, sends an API request. Print its response on console. Parse the API response to JSON and print JSON response in console. Also it validates the data in JSON using the JSON path
Pre-requistics
1. An API url. Here we use the url https://reqres.in/api/users?page=2. Below is the API response
```xml
{"page":2,"per_page":3,"total":12,"total_pages":4,"data":[{"id":4,"email":"eve.holt@reqres.in","first_name":"Eve","last_name":"Holt","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/marcoramires/128.jpg"},{"id":5,"email":"charles.morris@reqres.in","first_name":"Charles","last_name":"Morris","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/stephenmoon/128.jpg"},{"id":6,"email":"tracey.ramos@reqres.in","first_name":"Tracey","last_name":"Ramos","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/bigmancho/128.jpg"}]}
```
2. JSON formatter. Go to this site https://jsonformatter.curiousconcept.com/ and enter the API response to format to JSON.
   After converting to JSON:
```json
{  
   "page":2,
   "per_page":3,
   "total":12,
   "total_pages":4,
   "data":[  
      {  
         "id":4,
         "email":"eve.holt@reqres.in",
         "first_name":"Eve",
         "last_name":"Holt",
         "avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/marcoramires/128.jpg"
      },
      {  
         "id":5,
         "email":"charles.morris@reqres.in",
         "first_name":"Charles",
         "last_name":"Morris",
         "avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/stephenmoon/128.jpg"
      },
      {  
         "id":6,
         "email":"tracey.ramos@reqres.in",
         "first_name":"Tracey",
         "last_name":"Ramos",
         "avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/bigmancho/128.jpg"
      }
   ]
}
```
3. The package 'jsonpath' to validate the json path .
   * Open cmd and type 'pip install jsonpath'
   * On pycharm, go to project -> settings -> project name -> project interperter -> install jsonpath module
  
Steps in the program
1. import requests module. Request module is used to send request to API
2. import json module, as we need json functions to work with
3. import jsonpath module, as we need to validate the json path
4. using requests get method get the response from API, save it an object and print it in the console
5. check the status code using the assertion method. If the status code is 200, go ahead with the execution
6. using json loads function, parse the API response to json format, save it an object and print it in the console
7. Apply the jsonpath we need to validate. the syntax is ```python jsonpath.jsonpath(json_response,'jsonpath')```
   jsonpath is a method in jsonpath module
   
```python
#import request module, since we need to send request to API
import requests
#import json module,as we need to work with json
import json
#import jsonpath module. This is not present by default. Go to command prompt and install. This module is to validate the JSON path
import jsonpath

#API using https://reqres.in/api/users?page=2
#make a request to API. Whatever response store it in response1
api_url="https://reqres.in/api/users?page=2"
response1=requests.get(api_url)

#Print the response
print("the response from API is as below :")
print(response1.text)

#Validate status code. We are checking using assertion if the status code is 200. If it is true, it executes the remaining code. If not it pass an assertion error
assert response1.status_code==200

#Suppose we if we check for status code==201, it throws an assertion error
# assert response1.status_code==201

#parse the response to JSON,by using json loads function. Save it in json_result object
json_response=json.loads(response1.text)
print("After parsing the API response to JSON is as below: ")
print(json_response) #The response in JSON format is displayed on console

#Validate the response by using the jsonpath. 
#Apply the jsonpath to validate
#jsonpath module has jsonpath function
#syntax jsonpath.jsonpath(json_response,'jsonpath')
#jsonpath for finding the value in the key 'total'
x= jsonpath.jsonpath(json_response,'total')
print("the value in the json path total: "+ str(x)) #Here the value displays in array like [12]
#to display the value in list
print("the value in the json path total: "+ str(x[0]))

#Validate data in first_name in data array. the object data has 3 arrays. To get the data from the first array, pass the index 0
y = jsonpath.jsonpath(json_response,'data[0].first_name')
print("the value in the json path first_name: "+ str(y[0]))

#Validate data in the last data array
z = jsonpath.jsonpath(json_response,'data[2]')
print("the value in the json path in data array: "+ str(z[0]))

#If we want to fetch any value inside the data array. Suppose here data has 3 arrays and in each array first_name , last_name values are there. Suppose we want first_name from all the array
for val in json_response['data']: #This loops iterate to data arrays and find the first_name
    print(val['first_name'])
```
Program output:

```powershell
the response from API is as below :
{"page":2,"per_page":3,"total":12,"total_pages":4,"data":[{"id":4,"email":"eve.holt@reqres.in","first_name":"Eve","last_name":"Holt","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/marcoramires/128.jpg"},{"id":5,"email":"charles.morris@reqres.in","first_name":"Charles","last_name":"Morris","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/stephenmoon/128.jpg"},{"id":6,"email":"tracey.ramos@reqres.in","first_name":"Tracey","last_name":"Ramos","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/bigmancho/128.jpg"}]}

After parsing the API response to JSON is as below: 
{'page': 2, 'per_page': 3, 'total': 12, 'total_pages': 4, 'data': [{'id': 4, 'email': 'eve.holt@reqres.in', 'first_name': 'Eve', 'last_name': 'Holt', 'avatar': 'https://s3.amazonaws.com/uifaces/faces/twitter/marcoramires/128.jpg'}, {'id': 5, 'email': 'charles.morris@reqres.in', 'first_name': 'Charles', 'last_name': 'Morris', 'avatar': 'https://s3.amazonaws.com/uifaces/faces/twitter/stephenmoon/128.jpg'}, {'id': 6, 'email': 'tracey.ramos@reqres.in', 'first_name': 'Tracey', 'last_name': 'Ramos', 'avatar': 'https://s3.amazonaws.com/uifaces/faces/twitter/bigmancho/128.jpg'}]}

the value in the json path total: [12]
the value in the json path total: 12
the value in the json path first_name: Eve
the value in the json path in data array: {'id': 6, 'email': 'tracey.ramos@reqres.in', 'first_name': 'Tracey', 'last_name': 'Ramos', 'avatar': 'https://s3.amazonaws.com/uifaces/faces/twitter/bigmancho/128.jpg'}

First name from all the arrays:
Eve
Charles
Tracey
```

## Project 2 : RESTful API testing using Python
### Pre-requistics for this project
1. Modules needed
* requests
* json
* json path
In the above sections, we have already installed these packages through command prompt with command 'pip install packagename'.
2. The API site, from where we get the free API's. https://reqres.in/
   Here you can see list of many API's. Select any one and get the request
   Example : There is an API with name List Users and request is '/api/users?page=2'. Append this with the main URL
   https://reqres.in/api/users?page=2
   API :
   ```xml
   {"page":2,"per_page":3,"total":12,"total_pages":4,"data":[{"id":4,"email":"eve.holt@reqres.in","first_name":"Eve","last_name":"Holt","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/marcoramires/128.jpg"},{"id":5,"email":"charles.morris@reqres.in","first_name":"Charles","last_name":"Morris","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/stephenmoon/128.jpg"},{"id":6,"email":"tracey.ramos@reqres.in","first_name":"Tracey","last_name":"Ramos","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/bigmancho/128.jpg"}]}
   ```

3. On pycharm create a new project and check with the modules requests,json and json path are present.
   For that go to File -> Settings -> Project name -> Project interperter
    If not present search for the packages and install it.

4. Basic understandigg of Restful API and its methods
   A RESTful API is an application program interface (API) that uses HTTP requests to GET, PUT, POST and DELETE data. 
   RESTful APIs enable you to develop any kind of web application having all possible CRUD (create, retrieve, update, delete) operations. 
   Get - to send requests to server
   Post - to create new resources in the server
   Put - to update the existing resources
   Delete - to delete the resources in the server

### GET request method
GET method, is used to send the request to API. We get a response from the API after passing the get method.
In this, we are going to write a code to send a request to API, to pick the response and display on the console
Methods used :
* get - to get the response from the API
* content - To print the response body in bytes
* text - To print the response body in unicode
* header - To print the header of the response
  The response headers can give you useful information,such as the content type of the response payload and a time limit on how long to cache the response.

```python
#Requests module for sending request to API
import requests

#store the api url in an object
api_url ="https://reqres.in/api/users?page=2"

#Get method to get the response from the API. And store the response in an object
response = requests.get(api_url)

#To print the response body
#To see the response in bytes , you can see content method
print("Display the response in bytes: ")
print(response.content)

#To see the response in the form of unicode, you can see text method
print("Display the response in unicode : ")
print(response.text)

#To see the headers of the response
print("Display the header of the response: ")
print(response.headers)
```

Program output:
```powershell
Display the response in bytes: 
b'{"page":2,"per_page":3,"total":12,"total_pages":4,"data":[{"id":4,"email":"eve.holt@reqres.in","first_name":"Eve","last_name":"Holt","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/marcoramires/128.jpg"},{"id":5,"email":"charles.morris@reqres.in","first_name":"Charles","last_name":"Morris","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/stephenmoon/128.jpg"},{"id":6,"email":"tracey.ramos@reqres.in","first_name":"Tracey","last_name":"Ramos","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/bigmancho/128.jpg"}]}'

Display the response in unicode : 
{"page":2,"per_page":3,"total":12,"total_pages":4,"data":[{"id":4,"email":"eve.holt@reqres.in","first_name":"Eve","last_name":"Holt","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/marcoramires/128.jpg"},{"id":5,"email":"charles.morris@reqres.in","first_name":"Charles","last_name":"Morris","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/stephenmoon/128.jpg"},{"id":6,"email":"tracey.ramos@reqres.in","first_name":"Tracey","last_name":"Ramos","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/bigmancho/128.jpg"}]}

Display the header of the response: 
{'Date': 'Wed, 24 Jul 2019 07:24:13 GMT', 'Content-Type': 'application/json; charset=utf-8', 'Transfer-Encoding': 'chunked', 'Connection': 'keep-alive', 'Set-Cookie': '__cfduid=d24b075e3d645dfed0be516449e931a731563953053; expires=Thu, 23-Jul-20 07:24:13 GMT; path=/; domain=.reqres.in; HttpOnly; Secure', 'X-Powered-By': 'Express', 'Access-Control-Allow-Origin': '*', 'Etag': 'W/"21c-V3l8h04l5/8zLV+i3u8GJo8G3Y8"', 'Via': '1.1 vegur', 'CF-Cache-Status': 'HIT', 'Age': '1941', 'Expires': 'Wed, 24 Jul 2019 11:24:13 GMT', 'Cache-Control': 'public, max-age=14400', 'Expect-CT': 'max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"', 'Vary': 'Accept-Encoding', 'Server': 'cloudflare', 'CF-RAY': '4fb42736d9bec928-HYD', 'Content-Encoding': 'gzip'}
```

### Validate status code
A status code informs you of the status of the request.
Some of the status code and its status are:
200 OK - request successful
404 NOt found - resourse you are looking was not found
This URL has the complete list of status codes - https://en.wikipedia.org/wiki/List_of_HTTP_status_codes

```python
#Requests module for sending request to API
import requests

#store the api url in an object
api_url ="https://reqres.in/api/users?page=2"

#Get method to get the response from the API. And store the response in an object
response = requests.get(api_url)

#To validate the status code of the API
#By accessing .status_code, you can see the status code that the server returned
print(response.status_code)

#Sometimes, you might want to use this information to make decisions in your code
if response.status_code == 200:
    print("Success")
else:
    print("not successful")
```
Program output:

```powershell
C:\Work\APIAutomation\venv\Scripts\python.exe C:/Work/APIAutomation/GetRequest/GetPickDisplayResponse.py
200
Success
```

### To fetch response header values
1. Fetch the entire response header
2. Fetch specific response header value
3. Fetch cookies
4. Fetch encoding
5. Fetch elapsed time

```python
#Requests module for sending request to API
import requests

#store the api url in an object
api_url ="https://reqres.in/api/users?page=2"

#Get method to get the response from the API. And store the response in an object
response = requests.get(api_url)

#fetch response headers
#all header values are fetched
print("Fetch all the header values")
print(response.headers)

#if we want to fetch only specific values in the header
#to fetch date in header
print("Fetch the date from header:")
print(response.headers.get('Date'))

#to fetch the server value in header
print("Fetch the server value from header:")
print(response.headers.get('Server'))

#to fetch cookies in the response
print("Fetch cookies in the response: ")
print(response.cookies)

#To fetch encoding
print("Fetch encoding in the response: ")
print(response.encoding)

#to fetch the elapsed time.
#time taken between the request send and the response received
print("Fetch elapse time :")
print(response.elapsed)
```

Program output:

```powershell
Fetch all the header values
{'Date': 'Wed, 24 Jul 2019 15:18:45 GMT', 'Content-Type': 'application/json; charset=utf-8', 'Transfer-Encoding': 'chunked', 'Connection': 'keep-alive', 'Set-Cookie': '__cfduid=d9768759f19bf2f31c9f0a8febb07f3241563981525; expires=Thu, 23-Jul-20 15:18:45 GMT; path=/; domain=.reqres.in; HttpOnly; Secure', 'X-Powered-By': 'Express', 'Access-Control-Allow-Origin': '*', 'Etag': 'W/"21c-V3l8h04l5/8zLV+i3u8GJo8G3Y8"', 'Via': '1.1 vegur', 'CF-Cache-Status': 'HIT', 'Age': '1085', 'Expires': 'Wed, 24 Jul 2019 19:18:45 GMT', 'Cache-Control': 'public, max-age=14400', 'Expect-CT': 'max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"', 'Vary': 'Accept-Encoding', 'Server': 'cloudflare', 'CF-RAY': '4fb6de561e6ac94c-HYD', 'Content-Encoding': 'gzip'}

Fetch the date from header:
Wed, 24 Jul 2019 15:18:45 GMT

Fetch the server value from header:
cloudflare

Fetch cookies in the response: 
<RequestsCookieJar[<Cookie __cfduid=d9768759f19bf2f31c9f0a8febb07f3241563981525 for .reqres.in/>]>

Fetch encoding in the response: 
utf-8

Fetch elapse time
0:00:00.139789
```
### Fetch response content using JSON path
We have explained this on detail on the JSON section. 

```python
#Requests module for sending request to API
import requests
#import json module to parse the response to json format
import json
#import jsonpath to fetch content from response using jsonpath
import jsonpath

#store the api url in an object
api_url ="https://reqres.in/api/users?page=2"

#Get method to get the response from the API. And store the response in an object
response = requests.get(api_url)

#If you want to fetch any specific value in the response content
#Parse the response to JSON format
json_response = json.loads(response.text)
print(json_response)

#fetch specific content by JSONpath
#fetch the content in 'total_pages'
pages = jsonpath.jsonpath(json_response,'total_pages')
print(pages[0]) # the value is 4
#using assert we can compare the data
assert pages[0] ==4  #if true it does not display any thing. If you give wrong value, assertion error occurs.
```
Program output:

```powershell
{'page': 2, 'per_page': 3, 'total': 12, 'total_pages': 4, 'data': [{'id': 4, 'email': 'eve.holt@reqres.in', 'first_name': 'Eve', 'last_name': 'Holt', 'avatar': 'https://s3.amazonaws.com/uifaces/faces/twitter/marcoramires/128.jpg'}, {'id': 5, 'email': 'charles.morris@reqres.in', 'first_name': 'Charles', 'last_name': 'Morris', 'avatar': 'https://s3.amazonaws.com/uifaces/faces/twitter/stephenmoon/128.jpg'}, {'id': 6, 'email': 'tracey.ramos@reqres.in', 'first_name': 'Tracey', 'last_name': 'Ramos', 'avatar': 'https://s3.amazonaws.com/uifaces/faces/twitter/bigmancho/128.jpg'}]}
4
```
### Delete requests method
The delete() method sends a DELETE request to the specified url. DELETE requests are made for deleting the specified resource (file, record etc).
Go to https://reqres.in/ and you can see an API's in DELETE method. Its status code is 204 NOT FOUND.
API url is https://reqres.in/api/users/2
```xml
{"data":{"id":2,"email":"janet.weaver@reqres.in","first_name":"Janet","last_name":"Weaver","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/josephstein/128.jpg"}}
```
When you call the delete method and check for the status, you will get the status code 204
```python
import requests
api_url ="https://reqres.in/api/users/2"
#Delete method to delete the resources in the server
response=requests.delete(api_url)
print(response.text) #No response is printed, as this is deleted
print(response.status_code) #Thisprints the status code as 204
```
Program output:
```powershell
204
```

### Post requests method
post method is used for creating a new resource in the server.The status code 201 means the resource is created in the server.
Pre-requistics
1. API url with POST status
Go to https://reqres.in/ and you can see several API's in post status. 
I have selected one and its URL is 'https://reqres.in/api/users'
```xml
{"page":1,"per_page":3,"total":12,"total_pages":4,"data":[{"id":1,"email":"george.bluth@reqres.in","first_name":"George","last_name":"Bluth","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/calebogden/128.jpg"},{"id":2,"email":"janet.weaver@reqres.in","first_name":"Janet","last_name":"Weaver","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/josephstein/128.jpg"},{"id":3,"email":"emma.wong@reqres.in","first_name":"Emma","last_name":"Wong","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/olegpogodaev/128.jpg"}]}
```
2. Create a json file with the request content on your system. Use notepad++ and in json format enter the resource to be added. And save it as json file.
   Example:
   ```json
   {
    "name": "Anusha",
    "job": "Tester",
	"Age":30
    }
    ```

Steps in the program
1. Import requests module,json and json path
2. Open the json file saved in your system in read mode
3. By file read method, read the complete data from the json file
4. To parse this file to json format by using json loads method and save it in a object
5. Make a post request. While making a post request you need to send the url and the request body. Save tthe response from post method in an object
   syntax : requests.post(url,request body)
6. Print the response.It has created a resource. That message is displayed on the screen. Also if you check the status code you will get 201(Resource created)

```python
import requests
import json

api_url = "https://reqres.in/api/users"

#Open the json file from the system in read mode
#This file contains the data to be created in the resource
file1=open('C://Work/JSONFile.json','r')
#Read complete content from the inputfile to an object
json_input=file1.read()
#Parse the input file to json format
json_request=json.loads(json_input)

#Use the post method to create the resource
#When we use POST or PUT, we need to send request body and the URL
response=requests.post(api_url,json_request)
print(response.content)
print(response.status_code) #The status code is 201(resource created)
```

Program output:

```powershell
b'{"name":"Anusha","job":"Tester","Age":"30","id":"398","createdAt":"2019-07-25T05:15:01.387Z"}'
201
```

The below program creates a new resource to the server, parse the response to json to find the json path
```python
import requests
import json
import jsonpath

api_url = "https://reqres.in/api/users"

#Open the json file from the system in read mode
#This file contains the data to be created in the resource
file1=open('C://Work/JSONFile.json','r')
#Read complete content from the inputfile to an object
json_input=file1.read()
#Parse the input file to json format
json_request=json.loads(json_input)

#Use the post method to create the resource
#When we use POST or PUT, we need to send request body and the URL
response=requests.post(api_url,json_request)
print(response.content)
print(response.status_code) #The status code is 201(resource created)

assert response.status_code==201

#Fetch header from response
print(response.headers)
#To fetch content length from the header
print(response.headers.get('Content-Length'))

#Parse response to json
response_json=json.loads(response.text)

#in the response we need to validate the json path for id
#Everytime your running, you get a new id as a new resource is created on each run
x=jsonpath.jsonpath(response_json,'id')
print(x[0])
```
Program output:
```powershell
b'{"name":"Anusha","job":"Tester","Age":"30","id":"156","createdAt":"2019-07-25T05:31:01.510Z"}'

201

{'Date': 'Thu, 25 Jul 2019 05:31:01 GMT', 'Content-Type': 'application/json; charset=utf-8', 'Content-Length': '93', 'Connection': 'keep-alive', 'Set-Cookie': '__cfduid=d4a88c2f18f7e6530dd546759c0040faf1564032661; expires=Fri, 24-Jul-20 05:31:01 GMT; path=/; domain=.reqres.in; HttpOnly; Secure', 'X-Powered-By': 'Express', 'Access-Control-Allow-Origin': '*', 'Etag': 'W/"5d-724KUGdZaG8Bk0kPSt6fNu7+E4Y"', 'Via': '1.1 vegur', 'Expect-CT': 'max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"', 'Server': 'cloudflare', 'CF-RAY': '4fbbbec4bb9ecb21-HYD'}

93

{'name': 'Anusha', 'job': 'Tester', 'Age': '30', 'id': '156', 'createdAt': '2019-07-25T05:31:01.510Z'}

156
```
### PUT requests method
Puts method, to update the resource on the server. Once put method is done, the status code of the reponse should be 200.

Pre-requistics
1. API url with PUT status
Go to https://reqres.in/ and you can an API UPDATE in PUT status. 
The URL is 'https://reqres.in/api/users/2'
```xml
{"data":{"id":2,"email":"janet.weaver@reqres.in","first_name":"Janet","last_name":"Weaver","avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/josephstein/128.jpg"}}
```
2. On the previous section to create a resource using POST method, we have create sa json file with the request content and saves as json file in the system. Open the same file, and update some data
   Example:
   ```json
   {
    "name": "Anusha updated",
    "job": "Tester updated",
	"Age":30
    }
    ```
Steps in the program
1. Import requests module,json and json path
2. Open the updated json file saved in your system in read mode
3. By file read method, read the complete data from the json file
4. To parse this file to json format by using json loads method and save it in a object
5. Make a PUT request. As post method, you need to send the URL and the request body. Save the response from post method in an object
   syntax : requests.put(url,request body)
6. Print the response.It has updated the existing resource. That message is displayed on the screen. Also if you check the status code you will get 200.
7. Parse the response to json and print the json response

```python
import requests
import json
import jsonpath
api_url = "https://reqres.in/api/users"
#Open the updated json file from the system in read mode
#This file contains the data to be created in the resource
file1=open('C://Work/JSONFile.json','r')
#Read complete content from the inputfile to an object
json_input=file1.read()
#Parse the input file to json format
json_request=json.loads(json_input)

#Use the put method to create the resource
#When we use POST or PUT, we need to send request body and the URL
response=requests.put(api_url,json_request)
print(response.content)
print(response.status_code) #The status code is 201(resource created)

assert response.status_code==200

#Parse response to json
response_json=json.loads(response.text)
print(response_json)
```

program output:

```powershell
b'{"name":"Anusha updated","job":"Tester updated","Age":"30","updatedAt":"2019-07-25T05:55:45.740Z"}'
200
{'name': 'Anusha updated', 'job': 'Tester updated', 'Age': '30', 'updatedAt': '2019-07-25T05:55:45.740Z'}
```

## Project 3: Web application automation using selenium
Prerequistes
* Install python(already done)
* Install pycharm or any other editor(already done)
* Install selenium package : pip install selenium

For practice the url used 'http://thetestingworld.com/testings/'
Go to pycharm,create a project and install the selenium package over there.
Files -> Settings -> project name -> project interperter -> install selenium

### Test case
* Open browser
* Enter URL
* Maximize the browser
* Enter data in to textbox
* Click on radio button
* Click on checkbox
* click on the link
* select from dropdown list
* close the browser

Program
1. import class Chrome from the selenium webdriver module, as we are going to work on chrome browser
2. import select class from selenium, as we need to create object for select for dropdown selection
3. call the chrome driver
    we need a software(exe file) which works as  a bridge between the browser and our test case.
    For this we need chromedriver.exe file. Download it from 'http://chromedriver.chromium.org/downloads'
    #Two approaches to use this:
     * download the exe file in the location to your python scripts folder 'C:\Python\Python37-32\Scripts' 
     * in the program give the path where you saved the exe file in your system
        path ='c\\......\\chromedriver.exe
        driver=Chrome(executable_path=path)
4. by get method enter the url,where you want to work
5. using chrome inspect(rightclick on the element and inspect), the elements of the webpage to get its html code
6. enter data to the boxes,by sendkeys method
7. click on the button by click method
8. check radiobuttons
9. check checkboxes
10. work on dropdown
    Difference with dropdown and list is, we can select only one value from dropdown, where on list you can select multiple values
    When you inspect an dropdown element, the html tag should start with select
    We can use three methods index,value and visible text to select from dropdown

```python
#import class with the name chrome
from selenium.webdriver import Chrome
#import select class
from selenium.webdriver.support.select import Select

#Create object of the class chrome
driver=Chrome()

#get method to get url
driver.get("http://thetestingworld.com/testings/")

#maximize the window
driver.maximize_window()

#Enter data to the text boxes
driver.find_element_by_name('fld_username').send_keys('hello')
driver.find_element_by_xpath("//input[@name='fld_email']").send_keys('abc@gmail.com')
driver.find_element_by_name('fld_password').send_keys('hello')
driver.find_element_by_name('fld_cpassword').send_keys('hello')
#If you want to clear the first username and enter another
driver.find_element_by_name('fld_username').clear()
driver.find_element_by_name('fld_username').send_keys('goodmorning')

#working on radiobutton
driver.find_element_by_xpath("//input[@value='home']").click()

#working on the checkbox
driver.find_element_by_name('terms').click()

#to work on dropdown
#create object of the select
obj =Select(driver.find_element_by_name('sex'))
#we can select, using three methods index,value and visible text
#obj.select_by_index(1)
#obj.select_by_value("2")  #Value is a string
obj.select_by_visible_text("Male")

#Working on button .To click on submit
driver.find_element_by_xpath("//input[@type='submit']").click()

#Working on links
driver.find_element_by_link_text('Read Detail').click()

#close the browser
driver.close()
```
## Project -4 : Test data generation in python
We need a library for test data generation. That is faker library.
Faker is a Python package that generates fake data for you.
### Installation of faker library
* go to command prompt. Type pip install faker
* go to pycharm File -> settings -> Project name -> Project interpreter -> Install faker

### Faker methods
Faker has several methods to generate all kind of test data
Some of the methods are written under the below program:
Refer this site for more faker methods - http://zetcode.com/python/faker/

```python
#import faker module
from faker import Faker

#create object of the faker class
#The faker.Faker() creates and initializes a faker generator, which can generate data by accessing properties named after the type of data.
fakedata=Faker()
#faker has several methods to generate the fake data

#Faking names
print("Faking names")
print(fakedata.name())
print(fakedata.first_name())
print(fakedata.last_name())
print(fakedata.name_male())
print(fakedata.name_female())

#Faking job
print("Faking jobs")
print(fakedata.job())

#faking locale and personel data
print("faking personnel data")
print(fakedata.name())
print(fakedata.email())
print(fakedata.city())
print(fakedata.address())
print(fakedata.phone_number())

#faking currencies
print("faking currencies")
print(fakedata.currency())
print(fakedata.currency_name())
print(fakedata.currency_code())

#Faking words, sentence, text
print(fakedata.word())
print(fakedata.words(6))
print(fakedata.text())
print(fakedata.sentence())

#Faking internet related data
print(fakedata.hostname())
print(fakedata.domain_name())
print(fakedata.mac_address())

#Faking date and time
print(fakedata.date_of_birth())
print(fakedata.year())
```
  
Program output:

```python
Faking names
Lauren Moran
Lisa
Sandoval
Jonathan Chapman
Samantha Smith
Faking jobs
Chief Marketing Officer
faking personnel data
April Kelley
plopez@brown.biz
Lake Gailland
5489 Jackson Square Apt. 536
Jillland, HI 40357
+1-400-407-8652x04497
faking currencies
('XOF', 'West African CFA franc')
Guyanese dollar
JOD
better
['people', 'prove', 'water', 'town', 'window', 'usually']
Event while at. Receive heavy his many medical along act.
Computer certainly night available. Clear can as new. Account sister personal can film control government.
Shake interest think great.
db-98.dunn-johnson.com
ortiz.biz
88:5a:02:ae:50:f5
1948-10-17
1992
```
##3 Program to generate test data multiple times

```python
#import faker module
from faker import Faker

#create object of the faker class
fakedata=Faker()

#suppose we want to generate the above test data 10 times
for i in range(1,11):
    print(fakedata.name() + " " + fakedata.email() + " " + fakedata.city() + " " + fakedata.phone_number())
  
```

Program output:
```powershell
George Mooney PhD ronaldgomez@adams.org Lake Brittany 8103868877
Karen Ford robinsonmichael@hotmail.com Julianmouth 760.223.6602x44932
Jaime Tucker hughessarah@hotmail.com Youngberg 791-593-5127x56095
Dustin Becker dillonking@hart-harris.com North Lindseyland 034.522.9292x909
Richard Mann yjones@hotmail.com East Sandramouth 911.138.2044
Christie West justinjimenez@sexton-russell.net Port Michael 7985193124
Tammy Kennedy kathy63@gmail.com Wilsonhaven 581.264.6542x115
Courtney Hicks mcclainspencer@murphy.com Wardchester 424.220.5080x46313
Darren Thomas justin12@hotmail.com Port Breannashire 774-358-3306x101
Lauren Hernandez mcarter@yahoo.com New Nathanielland 252.777.5617x03522
```

### Program to write test data to excel sheet n number of times
```python
#import faker module
from faker import Faker
#import xlwt module to work in excel
import xlwt

#create object of the faker class
fakedata=Faker()

#to store the data in excel
workbook=xlwt.Workbook()
sheet=workbook.add_sheet("sheet1")
userNum=input("Enter the number of records needed:")
userNum=int(userNum)
for i in range(1,userNum):
    sheet.write(i,0,fakedata.name()) # in write method we are passing row, col and test data
    sheet.write(i,1,fakedata.email())
    sheet.write(i,2,fakedata.city())
    sheet.write(i,3,fakedata.random_number())
    sheet.write(i,4,fakedata.phone_number())
    sheet.write(i,5,fakedata.address())


workbook.save("C://Work/Result1.xls")
```

Program output: 
```powershell
Enter the number of records needed: 10
Open the Excel sheet in Result1.xls on the location "C://Work"
```
### Program to get user number of records and user choice of test data and write that to an excel sheet

BaseFile.py
```python
#import faker method
from faker import Faker
#import xlwt to work with xls file
import xlwt
#create the object of faker
fakedata=Faker()
#create the object of workbook
workbook=xlwt.Workbook()
#add sheet to workbook
sheet=workbook.add_sheet("sheet1")

#Function to display just the welcome message
def welcomeMessage():
    print("Welcome to test data generator")

#Function to prompt number of records from the user
def recordsFromUser():
    userNum=input("how many records user wanted-->")
    return userNum

#Function to prompt the user choice of test data
def listofOptions():
    print(" enter the options : 1 for name, 2 for email, 3 for address and 4 for phone number")
    userOp=input("Enter your choice -->")
    return userOp

#Function to generate test data and to write to excel sheet
def generateData(userNum,userOp):
    r=int(userNum)
    list1=userOp.split(",") #Split function as user can enter multiple choices like 1,2,3,4
    for i in range(0,r):
        for j in (list1):
            if(j=='1'):
                sheet.write(i,0,fakedata.name())
            elif(j=='2'):
                sheet.write(i,1,fakedata.email())
            elif(j=='3'):
                sheet.write(i,2,fakedata.address())
            elif(j=='4'):
                sheet.write(i,3,fakedata.phone_number())
    workbook.save("C://Work/FakeData.xls") #Save the excel sheet
```

ExecutionFile.py

```python
import BaseFile
BaseFile.welcomeMessage()
n=BaseFile.recordsFromUser() #This function returns the number of records while calling
o=BaseFile.listofOptions()#this function returns the user choice while calling
BaseFile.generateData(n, o) #pass record number and user option as parameteres
```
Program output:
```powershell
Welcome to test data generator
how many records user wanted-->100
 enter the options : 1 for name, 2 for email, 3 for address and 4 for phone number
Enter your choice -->1,2,3,4

Process finished with exit code 0
```
An excel sheet named 'FakeData.xls' will be created with 100 testdata of name,email,address and phonenumber in the location "C://Work"

Refer this site for more practical codes on data generation
https://www.geeksforgeeks.org/python-faker-library/









# Basics
### How to take input from user? 
For this we use input function and assign the vanlue to the appropriate variable. The return type of the input is string i.e whatever the input given by the user is stored in the variable in the form of string.


```python
variable1 = input("Type the input: ")
type(variable1)
```

    Type the input: 69
    str



In above example, we used input function and assigned the value to "variable1". 
Inside input function we use a string ["Type the input: "] that would be the prompt to the terminal i.e the message to which the user would respond with an input.

Now to convert the input to required data type we use type casting.
i.e int() -> for integer, 
float() -> for float, 
chr() -> for a character, 
str() -> for string [can be used to convert other data type to string form].


```python
variable1 = int(float(input("Enter the number: ")))
print(variable1)
```

    Enter the number: 69.96
    69
    

In The above example we used input function which gives the input in the form of string, then converted it to floating value, then to int. In the last step the decimal value is discarded. Note that the string can be directly converted to integer.

For output we use print function 

We could cluster and print multiple things separated by a comma (,)


```python
print("The intiger value of the number is",variable1,"which is not", 8.85)
```

    The intiger value of the number is 69 which is not 8.85
    

Note that the print function adds a space in between each element being printed

### Lists

list is a builtin datatype in python. It is used to store multiple data in a single variable. It is similar to array. The elements of lists are stored in [ ] . To create an empty list...


```python
list_name = []
```


```python
# A list with 3 integers
numbers = [1, 2, 5]

print(numbers)

# Output: [1, 2, 5] 
```

    [1, 2, 5]
    


```python
# list with mixed data types
my_list = [1, "Hello", 3.4]
```

To create a list of size n we cant copy the same as c++ or c. Insted we do this... where inside range is the number size of the list.


```python
my_list=list(range(5))
print(my_list)
```

    [0, 1, 2, 3, 4]
    

In Python, each item in a list is associated with a number. The number is known as a list index.

We can access elements of an array using the index number (0, 1, 2 …). For example,


```python
languages = ["Python", "Swift", "C++"]

# access item at index 0
print(languages[0])   # Python

# access item at index 2
print(languages[2])   # C++
```

    Python
    C++
    

#### Negative Indexing in Python
Python allows negative indexing for its sequences. The index of -1 refers to the last item, -2 to the second last item and so on.

Let's see an example,


```python
languages = ["Python", "Swift", "C++"]

# access last item 
print(languages[-1])   # C++
```

    C++
    

#### Add Elements to a Python List
Python List provides different methods to add items to a list.

##### 1. Using append()

The append() method adds an item at the end of the list. For example,


```python
numbers = [21, 34, 54, 12]

print("Before Append:", numbers)

# using append method
numbers.append(32)

print("After Append:", numbers)
```

    Before Append: [21, 34, 54, 12]
    After Append: [21, 34, 54, 12, 32]
    

##### 2. Using extend()

We use the extend() method to add all items of one list to another. For example,


```python
prime_numbers = [2, 3, 5]
print("List1:", prime_numbers)

even_numbers = [4, 6, 8]
print("List2:", even_numbers)

# join two lists
prime_numbers.extend(even_numbers)

print("List after append:", prime_numbers) 
```

    List1: [2, 3, 5]
    List2: [4, 6, 8]
    List after append: [2, 3, 5, 4, 6, 8]
    

#### Change List Items
Python lists are mutable. Meaning lists are changeable. And, we can change items of a list by assigning new values using = operator. For example,


```python
languages = ['Python', 'Swift', 'C++']

# changing the third item to 'C'
languages[2] = 'C'

print(languages)  # ['Python', 'Swift', 'C']
```

    ['Python', 'Swift', 'C']
    

#### Remove an Item From a List
##### 1. Using del()

In Python we can use the del statement to remove one or more items from a list. For example,


```python
languages = ['Python', 'Swift', 'C++', 'C', 'Java', 'Rust', 'R']

# deleting the second item
del languages[1]
print(languages) # ['Python', 'C++', 'C', 'Java', 'Rust', 'R']

# deleting the last item
del languages[-1]
print(languages) # ['Python', 'C++', 'C', 'Java', 'Rust']

# delete first two items
del languages[0 : 2]  # ['C', 'Java', 'Rust']
print(languages)
```

    ['Python', 'C++', 'C', 'Java', 'Rust', 'R']
    ['Python', 'C++', 'C', 'Java', 'Rust']
    ['C', 'Java', 'Rust']
    

##### 2. Using remove()

We can also use the remove() method to delete a list item. For example,


```python
languages = ['Python', 'Swift', 'C++', 'C', 'Java', 'Rust', 'R']

# remove 'Python' from the list
languages.remove('Python')

print(languages) # ['Swift', 'C++', 'C', 'Java', 'Rust', 'R']
```

    ['Swift', 'C++', 'C', 'Java', 'Rust', 'R']

For futher learning i reccomend this course [100-days-of-code](https://www.udemy.com/course/100-days-of-code/)
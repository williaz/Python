# Python

###Basics
#### Syntax
- A colon denotes the start of an indented code block after which all of the code must be indented by the same amount until the end of the block.
- is ignored by the Python interpreter => comment
- Functions can take both positional and keyword arguments
```
result = f(a, b, c, d=5, e='foo')

```
- Assignment is also referred to as binding, as we are binding a name to an object.
- object references in Python have no type associated with them.
- To check if two references refer to the same object, use the is keyword.
```
a is not c
```
```
a + b Add a and b
a - b Subtract b from a
a * b Multiply a by b
a / b Divide a by b
a // b Floor-divide a by b, dropping any fractional remainder
a ** b Raise a to the b power
a & b True if both a and b are True; for integers, take the bitwise AND
a | b True if either a or b is True; for integers, take the bitwise OR
a ^ b For booleans, True if a or b is True, but not both; for integers, take the bitwise EXCLUSIVE-OR
a == b True if a equals b
a != b True if a is not equal to b
a <= b, a < b True if a is less than (less than or equal) to b
a > b, a >= b True if a is greater than (greater than or equal) to b
a is b True if a and b reference the same Python object
a is not b True if a and b reference different Python objects
```

#### Scalar
- “single value” types
```
None The Python “null” value (only one instance of the None object exists)
str String type; holds Unicode (UTF-8 encoded) strings
bytes Raw ASCII bytes (or Unicode encoded as bytes)
float Double-precision (64-bit) floating-point number (note there is no separate double type)
bool A True or False value
int Arbitrary precision signed integer
```
- You can write string literals using either single quotes ' or double quotes "
- For multiline strings with line breaks, you can use triple quotes, either ''' or """
```
fval2 = 6.78e-5
```
- The backslash character \ is an escape character

- String objects have a format method that can be used to substitute formatted arguments into the string, producing a new string:

```
template = '{0:.2f} {1:s} are worth US${2:d}'
template.format(4.5560, 'Argentine Pesos', 1)
>>'4.56 Argentine Pesos are worth US$1'
```


- None is the Python null value type. If a function does not explicitly return a value, it implicitly returns None

```
from datetime import datetime, date, time
dt = datetime(2011, 10, 29, 20, 30, 21)
dt.strftime('%m/%d/%Y %H:%M')
>>'10/29/2011 20:30'

%Y Four-digit year
%y Two-digit year
%m Two-digit month [01, 12]
%d Two-digit day [01, 31]
%H Hour (24-hour clock) [00, 23]
%I Hour (12-hour clock) [01, 12]
%M Two-digit minute [00, 59]
%S Second [00, 61] (seconds 60, 61 account for leap seconds)
%w Weekday as integer [0 (Sunday), 6]
%U Week number of the year [00, 53]; Sunday is considered the first day of the week, and days before the first Sunday of
the year are “week 0”
%W Week number of the year [00, 53]; Monday is considered the first day of the week, and days before the first Monday of
the year are “week 0”
%z UTC time zone offset as +HHMM or -HHMM; empty if time zone naive
%F Shortcut for %Y-%m-%d (e.g., 2012-4-18)
%D Shortcut for %m/%d/%y (e.g., 04/18/12)
```
#### Control Flow

- if, elif, and else
```
if x < 0:
    print('It's negative')
elif x == 0:
    print('Equal to zero')
elif 0 < x < 5:
     print('Positive but smaller than 5')
else:
     print('Positive and larger than or equal to 5')
```

- for loops
- You can advance a for loop to the next iteration, skipping the remainder of the block, using the continue keyword.
- A for loop can be exited altogether with the break keyword.
```
for value in collection:
# do something with value

# if the elements in the collection or iterator are sequences
# (tuples or lists, say), they can be conveniently unpacked into variables in the for
# loop statement

for a, b, c in iterator:
# do something
```

- while
- pass: used in blocks where no action is to be taken
- range 
```
# range produces integers up to but not including the endpoint
list(range(0, 20, 2))
>>[0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
```
- A ternary expression in Python allows you to combine an if-else block that produces a value into a single line or expression.
```
'Non-negative' if x >= 0 else 'Negative'
>>'Non-negative'
```


### Data Structure

#### Tuple
- A tuple is a fixed-length, immutable sequence of Python objects.
- once the tuple is created it’s not possible to modify which object is stored in each slot
```
#The easiest way to create one is with a comma-separated sequence of values
tup = 4, 5, 6
tup
>>(4, 5, 6)

#You can convert any sequence or iterator to a tuple by invoking tuple
In [6]: tup = tuple('string')
In [7]: tup
Out[7]: ('s', 't', 'r', 'i', 'n', 'g')
In [8]: tup[0]
Out[8]: 's'

#using the + operator to produce longer tuples
In [13]: (4, None, 'foo') + (6, 0) + ('bar',)
Out[13]: (4, None, 'foo', 6, 0, 'bar')

In [14]: ('foo', 'bar') * 4
Out[14]: ('foo', 'bar', 'foo', 'bar', 'foo', 'bar', 'foo', 'bar')
#Note that the objects themselves are not copied, only the references to them.
```
- unpack
```
In [18]: tup = 4, 5, (6, 7)
In [19]: a, b, (c, d) = tup
In [20]: d
Out[20]: 7

#swap
In [21]: a, b = 1, 2
In [22]: a
Out[22]: 1
In [23]: b
Out[23]: 2
In [24]: b, a = a, b
In [25]: a
Out[25]: 2
In [26]: b
Out[26]: 1
```

- A common use of variable unpacking is iterating over sequences of tuples or lists:
```
In [27]: seq = [(1, 2, 3), (4, 5, 6), (7, 8, 9)]
In [28]: for a, b, c in seq:
....: print('a={0}, b={1}, c={2}'.format(a, b, c))
a=1, b=2, c=3
a=4, b=5, c=6
a=7, b=8, c=9
```

- *rest
```
In [29]: values = 1, 2, 3, 4, 4
In [30]: a, b, *_ = values
In [31]: a, b
Out[31]: (1, 2)
In [32]: _
Out[32]: [3, 4, 4]

values.count(4)
2
```







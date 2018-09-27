# Python

###Basics
#### Syntax
- A colon denotes the start of an indented code block after which all of the code must be indented by the same amount until the end of the block.
- # is ignored by the Python interpreter => comment
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




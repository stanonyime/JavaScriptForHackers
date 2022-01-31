# Data Types
JavaScript supports the following data 8 types:
 - number
 - bigint
 - string
 - boolean
 - undefined
 - null
 - object
 - symbol
 
 All types except objects define immutable values. The immutable types are called the **primitive data types*
## Number
Numbers in JavaScript are represented as double-precision 64-bit binary format IEEE-754 values. There are no integer types and no specific types for unsigned and signed numeric values. All numbers are floats

Examples:
12
12.5
-12 

Numbers can be represented in the following forms:
a) 1000
b) 1e3 
The two forms represent the same value 1000. 

**Number** is a wrapper object around JavaScript numbers whose constructor provides functions for conversions of strings to numbers. 

### Number limits
The highest precision possible in JavaScript numbers is 17 decimal places. Numbers range between -(2^53 − 1) and 2^53 − 1
The largest value a Number can hold is about 1.8E308 that is 1.8 x 10^308


Values higher than that are replaced with the special Number constant Infinity. In addition to representing floating-point numbers, the number type has three symbolic values: +Infinity, -Infinity, and NaN ("Not a Number").

To check for the largest available value or smallest available value within ±Infinity, you can use the constants 
Number.MAX_VALUE or 
Number.MIN_VALUE.
You can also check if a number is in the double-precision floating-point number range using Number.isSafeInteger() as well as Number.MAX_SAFE_INTEGER and Number.MIN_SAFE_INTEGER.

Beyond this range, integers in JavaScript are not safe anymore and will be a double-precision floating point approximation of the value.

The number 0 is represented as both -0 and +0. (0 is an alias for +0.)

In practice, this has almost no impact. For example, +0 === -0 is true. However, you are able to notice this when you divide by zero:
35 / +0 = Infinity
35 / -0 = -Infinity

# BigInt type
The BigInt type is a numeric primitive in JavaScript that can represent integers with arbitrary precision. With BigInts, you can safely store and operate on large integers even beyond the safe integer limit for Numbers.

A BigInt is created by appending n to the end of an integer or by calling the constructor.

You can obtain the largest safe value that can be incremented with Numbers by using the constant Number.MAX_SAFE_INTEGER. With the introduction of BigInts, you can operate with numbers beyond the Number.MAX_SAFE_INTEGER.

BigInts cannot be operated on interchangeably with Numbers. Instead a TypeError will be thrown.

# String
JavaScript's String type is used to represent textual data. It is a set of "elements" of 16-bit unsigned integer values. Each element in the String occupies a position in the String. The first element is at index 0, the next at index 1, and so on. The length of a String is the number of elements in it

# Null type
The Null type has exactly one value: null. See null and Null for more details.

# Undefined type
A variable that has not been assigned a value has the value undefined. See undefined and Undefined for more details.



# Symbol type
A Symbol is a unique and immutable primitive value and may be used as the key of an Object property

# Maps, Sets, WeakMaps, WeakSets
These data structures, introduced in ECMAScript Edition 6, take object references as keys. Set and WeakSet represent a set of objects, while Map and WeakMap associate a value to an object.

The difference between Maps and WeakMaps is that in the former, object keys can be enumerated over. This allows garbage collection optimizations in the latter case.

One could implement Maps and Sets in pure ECMAScript 5. However, since objects cannot be compared (in the sense of < "less than", for instance), look-up performance would necessarily be linear. Native implementations of them (including WeakMaps) can have look-up performance that is approximately logarithmic to constant time.

Usually, to bind data to a DOM node, one could set properties directly on the object, or use data- attributes. This has the downside that the data is available to any script running in the same context. Maps and WeakMaps make it easy to privately bind data to an object.
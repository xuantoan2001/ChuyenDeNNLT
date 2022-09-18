
# ChuyenDeNgonNguLapTrinh 
## Phạm Xuân Toán_1911505310155
#Ruby
#RubyMineIDE
### Mục lục

[0.Note](#Note)

[1. Reserved Words](#Reserved Words)

[2. Ruby Comments](#Ruby Comments)
- [2.1. Single-Line Comments](#Single-Line Comments)
- [2.2. Multi-Line Comments](#Multi-Line Comments)



===========================

# 0.Note
In Ruby, everything is treated as an object.


# 1.Reserved Words

The following list shows the reserved words in Ruby. These reserved words may not be used as constant or variable names. They can, however, be used as method names.

|Column1   |Column2 |Column3 |Column4     |
|----------|--------|--------|------------|
| BEGIN    | do	    | next	 | then       |
| END	   | else	| nil	 | true       |
| alias	   | elsif	| not	 | undef      |
| and	   | end	| or	 | unless     |
| begin	   | ensure	| redo	 | until      |
| break	   | false	| rescue | when       |
| case	   | for	| retry	 | while      |
| class	   | if	    | return | while      |
| def	   | in	    | self	 | \__FILE__  |
| defined? | module	| super	 | \__LINE__  |

# 2.Ruby Comments
Ruby comments:
- Single-Line Comments: start with a # character and run to the end of the line.
- Multi-Line Comments: start with the =begin token and ends with the =end token. 

Example:
#### 2.1. Single-Line Comments

```ruby
#This is a comment
```
#### 2.2. Multi-Line Comments
```ruby
=begin
This is a comment.
This is a comment, too1.
This is a comment, too2.
=end
```
# 3.Data Types
Data types in Ruby represents different types of data like text, string, numbers, etc. 
All data types are based on classes because it is a pure Object-Oriented language. 
There are different data types in Ruby as follows:
- Numbers
- Boolean
- Strings
- Hashes
- Arrays
- Symbols

#### 3.1. Numbers

- https://ruby-doc.com/docs/ProgrammingRuby/html/ref_c_numeric.html
- https://ruby-doc.com/docs/ProgrammingRuby/html/ref_c_bignum.html
- https://ruby-doc.com/docs/ProgrammingRuby/html/ref_c_fixnum.html
- https://ruby-doc.com/docs/ProgrammingRuby/html/ref_c_float.html
- https://ruby-doc.com/docs/ProgrammingRuby/html/ref_c_integer.html

Numbers: 
Generally a number is defined as a series of digits, using a dot as a decimal mark. 
Optionally the user can use the underscore as a separator. 
There are different kinds of numbers like integers and float. 
Ruby can handle both Integers and floating point numbers. 

According to their size, there are two types of integers, one is Bignum and second is Fixnum.

```ruby
# float type
price = 5.5

# both integer and float type
quantity = 3 
total = price * quantity
puts "The total bill is #{total} " 
```
Output: 
>The total bill is 16.5 

#### 3.1.1. Integers support several useful iterators
 **a)**
```
3.times        { print "X " }           >>Output: XXX
```
**b)**
```
1.upto(5)      { |i| print i, " " }     >>Output: 1 2 3 4 5
```
**c)**
```
99.downto(95)  { |i| print i, " " }     >>Output: 99 98 97 96 95 
```
**d)**
```
50.step(80, 5) { |i| print i, " " }     >>Output: 50 55 60 65 70 75 80 
```
#### 3.2. Boolean
Boolean: Data type represents only one bit of information either true or false.

```ruby
# Ruby program to illustrate the
# Boolean Data Type
 
if true
  puts "It is True!"
else
  puts "It is False!"
end

if 0
  puts "0 is True!"
else
  puts "0 is False!"
end
```
Output: 
>It is True! \
0 is True!

#### True, False, and Nil In Ruby
https://ruby-doc.com/docs/ProgrammingRuby/html/ref_c_trueclass.html
https://ruby-doc.com/docs/ProgrammingRuby/html/ref_c_falseclass.html
https://ruby-doc.com/docs/ProgrammingRuby/html/ref_c_nilclass.html

Always remember in Ruby true, false, and nil are objects, not numbers. 
Whenever Ruby requires a Boolean value, then nil behaves like false and values 
other than nil or false behave like true.
- Ruby does not contain Boolean class
- True is an object of TrueClass, false is an object of FalseClass

In Ruby, nil is a special value that denotes the absence of any value. 
Nil is an object of NilClass. Nil is Ruby’s way of referring to nothing or void

```ruby
# Checking for nil's class
a = nil.class
puts a       >> Output: NilClass
```
```ruby
# Ruby program to illustrate nil? method
# Checking for Nil
array = [ 1, 2, 3, 4, 5 ]
# Size array: 0->4

# Since array[5] does not exist so, it is nil.
result1 = array[5].nil?
puts result1

# Since array[2] exists so, it is not nil.
result2 = array[2].nil?
puts result2
```
Output:
>true \
false
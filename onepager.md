# Clny

# Comment

# Multi
  line
  comment

# Closed comment \#

# Type
Null # because CamelCased
print Null.cardinality # 1
print null # lowercase value assigned because type's cardinality is 1
debug Nulls # plural automatically created
help Null # 'type: "Null", 'is: false, 'to: .to\~, 'cardinality: 1

# Sum type
False
True
Bool: Boolean: False | True # alias
print Bool.cardinality # 2

Px: Pixel: 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7
  `suffix: "px"

# Number
## suffixes
## Infinity
## Filter to Int, UInt etc.

# String
## template string

# Match
## parser, Type

# Product type
Tuple: String, String # , for list
Point
  x: Px
  y: Px

# Exponential type
isPositive: Number => Bool n > 0
F: Number => Bool
f: F n => n > 0
f: String => Number ~.length

# Impure
a!: print "A"
a.impurity = 0

# Truthy
truthy?: null # truthy
if truthy print "Yes

# Throwable
divided^: 1 / 0
try divided print .

# Async
url: "http://www.example.com"
result@: fetch
when result print .

# State
state$: Point 1, 2 # mutable
when state print . # Observer
state.x = 2 # x: 2, y: 2

# Type functions
Strings<3> # 3 String's
Int: Numbers<~.isInteger> # filter
Even: Int<~ * 2> # map

# Regexes

# Miscellaneous
optional closing " { ( [
automatically toType, isType created
single values are also lists
automatic export
return, guard, throw
automatic return
print, debug, log, help
destructuring
object shorthand
ternary / infinary

# Syntax
# comment
   indent
-  indent
 application
: assignment
. self
~ argument
<> type function
() expression
{} scope
[] list
+ addition
- subtraction
* multiplication
/ division
% modulus
= equals
_ null
? truthy
^ throwable
@ async
$ state
! impurity
' convenience
\ escape
& and
` parser, regexes
| sum, or
, product, list
&: import
:& export

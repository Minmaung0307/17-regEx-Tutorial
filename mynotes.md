# Single Char

- \d 0-9 (d "lit-char" stands for digit, \ indicates the d is defined for digit)
- \w A-Za-z0-9 (w stands for word)
- \s whitespace (s stands for space or tab)
- . any char (. stands for whatsoever)

# Basic Quantifier

Quantifier modifies the previous char/s

- `.` any char
- `*` 0 or more
- `.*` any char and 0 or more (wildcard, meaning matching universe)
- `+` 1 or more
- `?` 0 or 1 (optionally)
- {min,max}
- {n}

# Position

- ^ beginning
- $ ending
- \b word boundry

# Char Class

- [ ]
- [abc]
- [_-.]
- l[yi]nk (lynk and link)
- \d{3}[-.]\d{3}[-.]\d{4} (123-456-7890 and 123.456.7890)
- \(?d{3}[-.)]\d{3}[-.]\d{4}

* (123) 456-7890 and any other phone numbers match

- Note: [a-z] from a to z
- [-.] - or .

?

- \(?d{3}[-.)]\d{3}[-.]\d{4}
- ^ negate
- [^abc]{3} negate
- [^0-5]{3} negate
- [a^bc] or

# Alternation

[\w.]+@\w+\.(net|com|edu)

- min@gmail.com
- min.123@gmail.net
- min_123@gmail.org

## literal char

## meta char

- 123-456-7890
- \d\d\d-\d\d\d-\d\d\d\d

# Capture Group

- \d{3}-\d{3}-\d{4}
- the 1st \d{3}- is group-0
- the 2nd \d{3}- is group-1
- the third \d{4}- is group-2

* step one

- \(?\d{3}[-.)]\d{3}[-.]\d{4}

* step two "add parenthesis"

- \(?(\d{3})[-.)]\d{3}[-.]\d{4}

* step three

- $1-xxx-xxxx

* last first flip
* zaw maung
* mar sue
* naing thant

- (\w+),\s+(\w+)
- $2 $1 "note $0 is for everything"
- replace all

* maung zaw
* sue mar
* thant naing

## senario

[Google](http://google.com) [test]
[itp](http://itp.nyu.edu)
[Coding Rainbow](http://codingrainbow.com)

- \[.\* matching anything, can put afteward
- \[.\*\] this will match the whole []()[]
- \[.\*?\] this will match only two brackets [][]

- \[(.\*?)]\((http.\*?)\)
- replace with
- `<a href="$2">$1</a>`

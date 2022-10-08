# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors have special meaning in regular expressions. They do not match any character. Instead, they match a position before or after characters:

- ^ – The caret anchor matches the beginning of the text.
- $ – The dollar anchor matches the end of the text.

```
let str = 'JavaScript';
console.log(/^J/.test(str));

let str = 'JavaScript';
console.log(/t$/.test(str));

let isValid = /^\d\d:\d\d$/.test('12:05');
console.log(isValid);
```

### Quantifiers

Quantifiers match a number of instances of a character, group, or character class in a string.

- Exact count {n}

A number in curly braces {n}is the simplest quantifier. When you append it to a character or character class, it specifies how many characters or character classes you want to match.

```
let str = 'ECMAScript 2020';
let re = /\d{4}/;

let result = str.match(re);

console.log(result);
```

- The range {n,m}

The range matches a character or character class from n to m times.

```
let str = 'The official name of ES11 is ES2020';
let re = /\d{2,4}/g;

let result = str.match(re);
console.log(result);
===============

let str = 'The official name of ES6 is ES2015';
let re = /\d{2,}/g;

let result = str.match(re);
console.log(result);
===============

let numbers = '+1-(408)-555-0105'.match(/\d{1,}/g);
console.log(numbers);
===============

let phone = "+1-(408)-555-0105";
let result = phone.match(/\d+/g);

console.log(result);
```

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

# Tutorial Matching URL

This file is intended to explain the details of how a specific regular expression works.  This particular 
expression we will explore is the a regular expression using regex of how the URL Matching validator and its components work.

## Summary

We will be evaluation the following regular expression used to match URL values:

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

Description bellow will provide details of the Anchors, Quantifiers, OR Operatios, Character Classes, Flags, Grouping and Capturing, Bracket Expressions, Greedy and Lazy Match, Boundaries, and Back-references, 

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

Code Snipet: `^,$`

Based on regular-expressions.info, they don't match any characters, anchors instead they match the position before, after and in between the characters.  

For instance in our regular expression: 

`^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

The caret `^` is in the begining of the expression to anchor the first group `(`.  While `$` is used at the end of the expression.

### Quantifiers

Based of the expression provided in this example, we can only find one that is the `?` in the expression this means that it would match zero to one time.  If you want to look more quatifiers, here are more expressions shown in [Microsoft](https://docs.microsoft.com/en-us/dotnet/standard/base-types/quantifiers-in-regular-expressions).

### OR Operator

In this expression that I am using, it doesn't contain any OR Operator but to breafly explain it, the OR Operator is when you have the `|` to indicate it could be either this expression or the other.  For instance, `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` is telling the expression that it could be either `[a-f0-9]{6}` or it could have `[a-f0-9]{3}`.

### Character Classes

Code Snippet: `[a-z\.]`

Based on regular-expressions.info, Character Classes or Set (whichever you like more) is to tell the regex engine to match only one of the serveral characters on the expression. For intance, in this code snipped that is provided above is telling the expression to look characters from `a` though `z`

### Flags

The expression that is presented for this code it doesn't have any flags but what flags does is a variable a variable defined "to have one value until some condition is true, in which case you change the variable's value".

### Grouping and Capturing

Groups and Capturing is when you put the parentheses `()` in everything in between is what the code is going to look for.  As for this code, it will take all of this expression `(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)`.

### Bracket Expressions

Expression: `[]`

Code Snippet: `[\da-z\.-]`

Bracket Expression are used to match any of the characters (either alphabetic, numeric, special characters, symbols etc..) that are defined within the brackets.

### Greedy and Lazy Match

Code Snippet: `([a-z\.]{2,6})`

Greedy match is when the code matches to the longest possible string of the expression while Lazy, is the opposite becuase it would match the the shortest possible string.  Some Greedy qualifiers on this code may be `+,0` while the lazy qualifiers on this code and is the most common one is th `?`.

### Boundaries

Boundaries works by matching everything that is in the middle of the expression.

Based on regular-expression.info, there are three different positions that qualify as word boundaries:

* Before the first character in the string, if the first character is a word character.
* After the last character in the string, if the last character is a word character.
* Between two characters in the string, where one is a word character and the other is not a word character.

### Back-references

Code Snippet: `[a-z\.]{2,6})([\/\w \.-]*`

Back-references based on regular-expressions.info, it matches the same text as previously match by capturing group.

As for this expression that we have,

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

The code will capture the string matched by `([a-z\.]{2,6})([\/\w \.-]*`

### Look-ahead and Look-behind

"Lookahead and lookbehind, collectively called “lookaround”, are zero-length assertions just like the start and end of line, and start and end of word anchors explained earlier in this tutorial." Links for more information [here](https://www.regular-expressions.info/lookaround.html).

## Author

This tutorial is brought you by Cristian Acevedo.  I am currently a student at UCF studing Full Stack Web Developer you can look at my Github page [here](https://github.com/cacevedo2011)

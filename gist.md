# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

I will be describing the functionality of the regex used to compare matching emails.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

Regex has many components, that are all wrapped between "/" characters.

### Anchors

There are two anchor characters, ^ and $. The ^ eaither indicates a specific word, or a range of characters that are displayed between brackets. The $ indicates the characters that the expression ends with, which can be a range or a specific string.

Both are present in the 'compare matching emails' regex, it starts with a ^ and ends with a $.

In the regex, the patterns being searched for are `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]`. These are all ranges within brackets.

### Quantifiers



### Grouping Constructs

### Bracket Expressions

A 'bracket expression' refers to the range of characters within two square brackets, this is also called a 'positive character group'. This can either have the exact characters listed out that should be included in the string (`[xyz]`) or it can be a range (`[x-z]`). The string only has to have one of the characters listed, it does not have to have all of the characters listed.

In the 'compare matching emails' regex, the ranges `a-z`, `0-9` and `a-z0-9_` are used. These are all lowercase, which means that only lowercase characters are being searched for.

`a-z` means that any lowercase letter in the alphabet between a and z is a valid input. 

`0-9` means that any numeric character between 0 and 9 is a valid input.

`a-z0-9_` means that any lowercase letter between a and z, any numeric character between 0 and 9, and the special character _ are all valid inputs.

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

# Regex - Matching an Email

Regex stands for 'regular expressions', which are groupings of specific characters that have specific meanings, and when compined can be used to define requirements for particular items. This allows for developers to easily put requirements on dynamic user inputs, where they want to allow a wide variety of inputs within specific parameters.

This can include usernames, passwords, emails, or any other regulated user input.

## Summary

I will be describing the functionality of the following regex for 'matching an email'. This regex defines the characters that can be used within each part of an email addess (username)@(subdomain).(top level domain). There are different options for each section.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

Regex has many components, that are all wrapped between "/" characters.

### Anchors

There are two anchor characters, `^` and `$`. The `^` eaither indicates a specific word, or a range of characters that are displayed between brackets. The `$` indicates the characters that the expression ends with, which can be a range or a specific string.

Both are present in the 'matching an email' regex, it starts with a `^` and ends with a `$`.

In the regex, the patterns being searched for are `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]`. These are all ranges within brackets.

### Quantifiers

Quantifiers define the limits on what a regex matches.

The quantifiers in the 'matching an email' regex are `{n,x}` and `+`.

`{2,6}` in the regex means that the length of the third section `([a-z\.]{2,6})` should be between two and six characters. It can not be greater than or less than that particular range. An example of this would be `dog`, `car` or `cheese`.

`+` is used in two different locations in the regex, `([a-z0-9_\.-]+)` and `([\da-z\.-]+)`. This means that, for both sections, there must be a match within the provided ranges one or more times. That means that `abcdef` or `aaaaaaa` are both valid options.

### Grouping Constructs

Parentheses are used to group constructs into sections also called 'subexpressions'. This allows different parts of the expression to have different requiremnts put on it.

There are three subexpressions in the 'matching an email' regex.

`([a-z0-9_\.-]+)` looks for at least one instance of characters that are either between a-z, 0-9, `.`, `-`, or `_`. `dog`, `dog.123`, and `ilike-dogs123_` are all valid combinations.


`([\da-z\.-]+)` looks for at least one instance of characters that are between a-z (defined explicetly) or 0-9 (defined by `\d`), `.` or `-`. `yahoo`, `gmail`, and `google` are all valid combinations.
 
`([a-z\.]{2,6})` looks for at least one instance of characters that are between a-z or a `.`, the number of characters has to be between 2 and 6. `com`, `net` and `eu` are all valid combinations.

### Bracket Expressions

A 'bracket expression' refers to the range of characters within two square brackets, this is also called a 'positive character group'. This can either have the exact characters listed out that should be included in the string (`[xyz]`) or it can be a range (`[x-z]`). The string only has to have one of the characters listed, it does not have to have all of the characters listed.

In the 'matching an email' regex, the ranges `a-z`, `0-9` and `a-z0-9_` are used. These are all lowercase, which means that only lowercase characters are being searched for.

`a-z` means that any lowercase letter in the alphabet between a and z is a valid input. `a`,`aaaa` or `abcdef` are all options.

`0-9` means that any numeric character between 0 and 9 is a valid input. `123` or `444456` are both inputs.

`a-z0-9_\.-` means that any lowercase letter between a and z, any numeric character between 0 and 9, and the special characters _, . or - are all valid inputs. `aaaaa`, `99999`, and `12-34.cats` all meet the requirements.

### Character Classes

Character classes are sets of characters that can be used to define additional character groups outside of the ranges.

The character classes used in this regex are `\d`.

`[\da-z\.-]` uses `\d` which means that any numeric character between 0-9 is a match. This means that `123abc` and `abccccc` are both matches.

### Character Escapes

A character escape is a `\` before another character, which tells regex to not take that character literaly.

In this regex, the character `.` is escaped in `([a-z0-9_\.-]+)` and `([\da-z\.-]+)`, which means that it is refering to the `.` character in all expressions, instead of the character class of `.` which means that all characters other than `\n` are a match. This means that `catsarefun` and `i.like.dogs` are both matches.

## Author

Madeline is a student at the University of Richmond coding bootcamp, with a passion for database design and a desire to learn.

https://github.com/m-r-urbanic
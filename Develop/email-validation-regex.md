# Regex gist

In this gist, I will explain the different components of a specific regular expression (regex) that validates an input as an email address. This will help a user understand how the regex works by breaking down the different components involved.

## Summary

The following is the regex I will break down to show how it works:
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
This regex makes sure an email is corrently entered. It does so by making sure an input matches a specific format. The format is, some number of lowercase letters, numbers, underscores, periods, or hyphens, followed by an @ symbol, followed by some number of numbers, letters, periods or hyphens, followed by a period, followed by 2 to 6 lowercase letters or periods.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
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

The anchors in this regex are the carrot top `^` and the dollar `$` symbols. 

The `^` indicates that it is the beginning of the expression. There cannot be any characters before the `^` or it won't be a match for the expression. The `$` indicates that it is the end of the expression. There cannot be any characters after the `$` or it won't be a match for the expression.

### Quantifiers

The quantifiers used in this regex are the plus `+` and the curly brackets `{}` symbols. 

The `+` indicates that there is one or more of the previous elements allowed. In the portion `([a-z0-9_\.-]+)`, the `+` indicates that there is one or more value(s) from the previous character class between the square brackets. The character class in this case are the characters of lowercase letters, digits 0-9, underscores, slashes, periods, or hyphens. The `+` in `([\da-z\.-]+)` indicates that there can be one or more digits, letters, periods, or dashes.

The `{}` indicates that there is a set number of characters. The `{2,6}` means that there are anywhere from 2 to 6 characters to be able to match from the character class. The `{2,6}` in `([a-z\.]{2,6})` means that there can be 2 to 6 letters or periods.

### Character Classes

The character class is defined by what is inside the square brackets `[]`. 

This regex has three character classes. The first character class is `[a-z0-9_\.-]`. This indicates that the letters a through z, the numbers zero through nine, the underscore, period, and hyphen are part of this character class.

The second character class is `[\da-z\.-]`. This indicates that the numbers zero through nine, letters a through z, period, and hyphen are part of this character class.

The final character class is `[a-z\.]`. This indicates that the letters a through z and a period are part of this character class.

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

https://github.com/JenGelfling

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

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
- [Grouping and Capturing](#grouping-and-capturing)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

The anchors in this regex are the caret top `^` and the dollar `$` symbols. 

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

### Grouping and Capturing

Grouping and capturing is defined by what is inside the round brackets `()`.

There is always a group zero, which is the complete regex.

Group one is `([a-z0-9_\.-]+)`. Group two is `([\da-z\.-]+)`. Group three is `([a-z\.]{2,6})`. This regex doesn't do anything with these groups, but does create groups that can be acted upon. So in an example, with an email of test@testing.com, where I want to replace the username/unique info "test" with XXX to hide it, I could user `XXX@$2.$3` to replace it.

### Greedy and Lazy Match

The quantifiers used in this regex, `+` and `{2,6}`, are both greedy. This means that they will try to match the maximum amount as opposed to the minimum amount.

## Author

My name is Ben and I have worked in the tech field for over a decade. I've recently started my coding journey by taking a full stack bootcamp and am excited to learn and understand how to build cool things. You can check out some of the things I've worked on at my [Github page](https://github.com/JenGelfling).

# Email address Matching

This tutorial is going to explain how regex matches characters to validate that the strign is Email, for this tutorial we are using `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. This regex can be useful when building a signup page for your application to prevent users from entering incorrect or false email addresses, or in a contact form to ensure that the email address is valid.

## Summary
This tutorial will demonstrate how regex matches each component to validate an Email.
Regex is used define patterns in a sequence characters; they can be used for anything like finding all the commas in a paragraph or to validate a string dosent contain innapropriate words. We tend to use regex to match patterns, validate user input and replace characters in a string. 

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
In this expression the following anchors are being used to match the email address.

The`^`anchor is used to indicate the start of a new string.

The `$` character is used to mark the end of the string.

### Quantifiers

Quantifiers are used to state how many characters you can expect in the given string.

The quantifiers in our expression are `+` and `{2,6}`.

In the folowing snippet of our expression `[a-z0-9_.-]+` is used to indicate that any string inside the brackeets is expected to come up atleast one time but not limited to one time.

The `[\da-z.-]+` part of the expression plays a similar role to the previous one.

`[a-z.]{2,6}` means that 2 to 6 characters from a-z are expected to appear. The 2 is used to mark the lower limit of characters and the 6 is used to mark the upper limit of characters.

### Character Classes

This expression only contains one character class, which is `\d`, this is used to match a single character that is a number from 0 to 9 and will only look for one digit unless specified otherwise.

The backslash is not used for anything other than to say that its not just a regular letter d. We could have also used the `.` character class to match any character but we wanted to specify a digit; this character class does not require a backslash.

### Grouping and Capturing

Parenthese are used to for grouping and capturing which means that anything within a set of parenthese is treated as a single group. The `([a-z0-9_\.-]+)` part of our regex is used to capture our email address and the `([\da-z\.-]+)` is used to capture the email type such as gmail or yahoo. The `([a-z\.]{2,6})`is responsible for capturing the ".com" section of our email address.

### Bracket Expressions

bracket expression are used to represent one character within the brackets. `[a-z0-9_\.-]` is matching a letter from a-z and expects a lower-case, matches any digit 0-9 or a period.

## Author

This tutorial was brought to you by Amado Cardenas and can be found on github as Amado-bot.
https://github.com/Amado-bot
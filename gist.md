# Match an Email - Regex Tutorial 

In this guide, we will explore how regular expressions (regex) can be employed to accurately match email addresses using the provided expression. `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. This becomes valuable when validating emails through technologies like Node.js (using packages like Inquirer) or MongoDB

## Summary

A regular expression is a sequence of characters that defines a pattern for searching within a text. It is extensively used to identify particular patterns within a larger body of text, facilitate find-and-replace tasks, or validate user input. In this tutorial, we will methodically examine the components of a regular expression and illustrate their significance in the context of matching email addresses.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
The anchors used in this regex expression for matching an email are `^ `, which indicates the beginning of the string and `$`to indicate the ending of the string. `(m)`, or multiline is not enabled, so the regex will end at `$`.

### Quantifiers
Quantifiers in this regex includes the `+` operator, which will connect the users email name + email service + `.com`. Another quantifier for this regex includes `{2,6}`, which will allow a match range of 2-6 characters for the character set of `[a-z\.]`.

### Character Classes
The character class in this expression is `\d`, which matches a single characters that is a digit from 0-9. It will only match a single digit such as "4", but not "44". 

### Grouping and Capturing
Capturing group #1 in this expression is `([a-z0-9_\.-]+)` that matches the user email name. The second capturing group is `([\da-z\.-]+)` which will match the email service. Then lastly, capture group #3 is `([a-z\.]{2,6})` to capture the `.com`.

### Bracket Expressions
Bracket expressions for email validation encompass character sets that are used to define specific patterns within the email: 
 * `[a-z0-9_\.-]`, which is matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters "_" , "-" , and ""; 
 * `[\da-z\.-]`, which is matching a single digit from 0-9, any character a-z (case senstive), and the characters "." and "-".; 
 * `[a-z\.]` matches any character a-z(case senstive) and the character ".". 

### Greedy and Lazy Match
This regrex includes greedy matches. Since it includes the `+` Quantifier, it will match as many times as possible giving back as needed. Another greedy Quantifier used in this regex is `{}` when matching `{2,6} for the last capture group.

## Felix Francisco
 
You can visit my GitHub profile [here](https://github.com/FelixFrancisco1776)



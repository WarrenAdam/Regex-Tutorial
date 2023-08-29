# Regex Tutorial: Email Matching

In this tutorial, we will learn the use of regular expressions (regex) to match emails using the expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. This can be useful for applications like MongoDb and Node, specifically inquirer.

## Summary

A regular expression or regex, is a sequence of characters that defines a search pattern. These sequence of characterss are a set set of strings matched to a given search pattern. What this means is it accepts a certain pattern of strings and reject other ones. A regex can consist of characters or metacharacters. A metacharcter indicates more generalized patterns as opposed to literal characters (i.e.; A, a, B, b etc.).

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping or Capturing Constructs](#grouping-or-capturing-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Matching](#greedy-and-lazy-matching)

## Regex Components

### Anchors

When matching an email, there are anchors for beginning midle and end of an expression. The anchors for the beginning is `^ `, at the end of string it is `$`. When a string is a multi-line, `(m)` will be shown. However if mutli-line is not indicated, it will signify like the end of a single-lined string with `$`.

### Quantifiers

For email matching, the quantifiers used in a regex are `+` and `{ , }`. The `+` operator refers to being a connector operator. For example, when you want to connect the user's email + the email service with `.com`. The `{ , }` operator is used to create a range to match between a certain number of charcaters. For example `{2,6}` will match a character range between 1 and 9 in a set of characters (i.e., `[a-z\.]`).


### Grouping or Capturing Constructs

 A grouping construct is also knowned within email regexes as capturing. A capturing group #1 in this expression is `([a-z0-9_\.-]+)` that matches the user email name. The second capturing group is `([\da-z\.-]+)` which will match the email service. Then lastly, capture group #3 is `([a-z\.]{2,6})` to capture the `.com`.

### Bracket Expressions

Bracket expressions for email matching includes the character sets of `[a-z0-9_\.-]`. In this example it is matching a set of letters specifically in the range of a-z and is case senstive. It also matches a character 0-9 and matches the characters "_" , "-" , and "."; `[\da-z\.-]`, which is matching a single digit from 0-9, any character a-z (case senstive), and the characters "." and "-".; `[a-z\.]` matches any character a-z(case senstive) and the character ".". 


### Greedy and Lazy Matching

This regrex includes greedy matches. Since it includes the `+` Quantifier, it will match as many times as possible giving back as needed. Another greedy Quantifier used in this regex is `{}` when matching `{2,6}` for the last capture group.

## Author

To view my projects and repositories head on over to https://github.com/WarrenAdam.
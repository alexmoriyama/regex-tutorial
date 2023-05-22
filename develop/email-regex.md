# Module 17 Homework

The purpose of this tutorial is to display a regex and thoroughly explain the search pattern. 

## Summary

In this regex, I have a snippet detailing a match for an email. Within this snippet I will detail how this regex breaks down the matching in order to properly match an email.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

In our regex, the anchors are both `^` and `$`. The `^` denotes the start of our string while the `$` anchor denotes the end of our string. Functionally, in our matching an email regex, the `^` is the start point for our string while the `$` is the end. 

### Quantifiers

Quantifiers tell our regex to match a specific amount of the character it is attached to, positioned to the left hand side. As an example, if we see `A+`, the quantifier will refer to the character `A`. If the quantifier lies outside of a paranthesis, than it will apply to the entirety of the subexpression within it. Another thing to note in our specific snippet is the brackets `{2,6}` which is quantifying that our sequence of characters is between 2-6. To put it simply, it is looking for the specific .com or .net after your email service provider.

### Character Classes

Character classes in this example would be `/d` which denotes a match for a single digit between 0-9. What it means in our second bracket expression is we can add a number from 0-9 on top of the string with letters a-z, a hyphen, and a period. This bracket expression is described in our code snippet as `[\da-z\.-]`


### Grouping and Capturing

Grouping in this code snippet is pretty clear. It is split into three components:

- `([a-z0-9_\.-]+)`: This is looking to match our username for our email.

- `([\da-z\.-]+)`: This is looking for our email service provider.

- `([a-z\.]{2,6})`: This is looking for the final .com/.net.


### Bracket Expressions

Bracket expressions are how you tell the regex engine you want the characters inside your brackets to match. As an example, if we had `[ab]` we would be looking for a string that contained either `a` or `b`. For this set of bracket expressions, the following would match: `aa`, `ba`, `abc`, `able`. Given the flexibility allotted in the previous example, we can add certain characters in our bracket expression to specify what would match. A hyphen `-` is commonly used between alphanumeric characters in order to present a range for that match. If we look at our code snippet for matching an email, we can see the examples `[a-z]` as well as `[0-9]` letting us know that any letter in the alphabet as well as any string 
with the numbers 0-9 will satisfy our code snippet.

Another important thing to note is that in bracket expression, if we add a `^` inside our bracket, we are denoting that it is a negative character group. If we include that in a bracket such as `[abc]` we would be looking for a string that doesn't include any of those 3 characters.

### Greedy and Lazy Match

A greedy quantifier is going to repeat as many times as possible as is denoted by the `+` symbol. Lazy mode is only going to look to repeat as minimally as possible and is denoted with a `?` but isn't included in our specific code snippet. We can see a greedy match in our first two groupings as referred to in the grouping and capturing section.

## Author

Alex Moriyama [My Github](https://github.com/alexmoriyama) [My LinkedIn](https://www.linkedin.com/in/alex-moriyama/)

# Regex Tutorial: Matching an email

This tutorial will instruct a user on how to use regular expression.

## Summary

Regular expressions, or regex for short, are a series of special characters that define a search pattern. Regular expressions are extremely useful in extracting information from any text by searching for one or more matches of a specific search pattern (i.e. a specific sequence of ASCII or unicode characters). In the below example, we'll dive into the pattern for validating email addresses. 

The regular expression to match name@email.com is: 

```
/^[a-zA-Z0-9.!#$%&’*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/
```

Here’s how it breaks down:
* The string can contain any lowercase or uppercase letter between a–z
* The string can contain any number between 0–9
* The string can contain these special characters: ! # $ % & ' * + - / = ? ^ _ ` { |
* The string can contain an @ symbol


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors
The characters ^ and $ are both Anchors.

The ^ anchor signifies a string that begins with the characters that follow it. 

```
^
```
The $ anchor signifies a string that ends with the characters that precede it. Just as with the ^ character, it can be preceded by an exact string or a range of possible matches.
```
$
```

### Quantifiers

Quantifiers determine the minimum and maximum number of characters that your regex matches, and look for as many occurrences or repetitions of a particular pattern that they can find. They include the following:

Matches the pattern zero or more times:
```
*
```
Matches the pattern one or more times:
```
+
```
Matches the pattern zero or one time:
```
?
```
Curly brackets can provide three different ways to set limits for a match:
```
{ n } Matches the pattern exactly n number of times

{ n, } Matches the pattern at least n number of times

{ n, x } Matches the pattern from a minimum of n number of times to a maximum of x number of times
```



### OR Operator

The OR Operator is a way to match one or multiple patterns. The pipe symbol (|) is used as an OR. Example:
```
(a|b|c) matches a, b, c, and cba
```

### Character Classes
A character class defines a set of characters, any one of which can occur in an input string to fulfill a match. Here are some of the other common character classes:

Matches any character except the newline character (\n)
```
. 
```
Matches any Arabic numeral digit. This class is equivalent to the bracket expression [0-9].
```
\d—
```
Matches any alphanumeric character from the basic Latin alphabet, including the underscore (_). This class is equivalent to the bracket expression [A-Za-z0-9_].
```
\w—
```
Matches a single whitespace character, including tabs and line breaks
```
\s
```
_Each of the last three character classes can be changed to perform an inverse match by capitalizing the letter character._


### Flags
Flags are placed at the end of a regex, and they define additional functionality or limits for the regex. These are the three you're most likely to encounter:
Global search: the regex should be tested against all possible matches in a string.
```
g
```
Case-insensitive search: case should be ignored while attempting a match in a string
```
i
```
Multi-line search: a multi-line input string should be treated as multiple lines
```
m
```

### Bracket Expressions
Bracket Expressions represents a range of characters that we want to match inside a set of square brackets ([]). 

The string can contain any lowercase letter between a–z. Keep in mind that this looks for lowercase characters only. If we wanted to include uppercase characters, we would need to change the expression to [a-zA-Z].
```
[a-z]
```
The string can contain any number between 0–9
```
[0-9]
```
The string can contain an underscore or hyphen. Both the underscore and the hyphen are called special characters. Special characters include any non-alphanumeric characters, such as punctuation or symbols. In this case, we only want a string that includes 
```
[! # $ % & ' * + - / = ? ^ _ ` { |] 
```

## Author

This tutorial was created by Jane Adams, a graduate from the UCLA Coding Bootcamp. Feel free to reach me at my [GitHub profile](https://github.com/janealexadams)! 

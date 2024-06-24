# REGEX TUTORIAL

This tutorial will show a detailed explanation of the regex used to validate email addresses, breaking down each component to help understand how it contributes to identifying valid email formats.

## Summary

This tutorial covers the regex pattern used to validate email addresses, ensuring they adhere to common standards:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This expression checks for a valid username, a domain name, and a domain extension, ensuring the email address is in a standard format.


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
Anchors (`^`, `$`) are used to match positions within the input string:
- `^` asserts the start of the string.
- `$` asserts the end of the string.

### Quantifiers
Quantifiers (`+`, `*`, `?`, `{n}`, `{n,}`, `{n,m}`) specify how many instances of a character or group must occur:
- `+` ensures one or more of the preceding element.
- `*` allows zero or more of the preceding element.
- `?` permits zero or one of the preceding element.

### OR Operator
The OR operator (`|`) allows for the matching of either the expression before or after it:
- `a|b` will match either 'a' or 'b'.

### Character Classes
Character classes allow matching any one character from a specific set:
- `[a-z0-9_\.-]` matches any lowercase letter, digit, underscore, or dot.
- `[\da-z\.-]` matches any digit, lowercase letter, dot, or hyphen.

### Flags
Flags modify the behavior of the regex search:
- `i` (case-insensitive): Makes the match case-insensitive.
- `g` (global): Ensures matching all occurrences.
- `m` (multi-line): Anchors apply to every line.

### Grouping and Capturing
Grouping (`()`) combines parts of the regex together, and capturing groups store data for later use:
- `([a-z0-9_\.-]+)` captures the username.
- `([\da-z\.-]+)` captures the domain name.
- `([a-z\.]{2,6})` captures the domain suffix.

### Bracket Expressions
Bracket expressions are used to include a set of characters to match:
- `[abc]` matches any single character a, b, or c.
- `[^abc]` matches any single character that is not a, b, or c.

### Greedy and Lazy Match
Greedy matches (`*`, `+`) grab as much as they can, while lazy matches (`*?`, `+?`) take as little as possible:
- `.*` is a greedy match, capturing as much as possible.
- `.*?` is a lazy match, capturing as little as possible.

### Boundaries
Boundaries (`\b`, `\B`) distinguish between words and non-word characters:
- `\b` represents a word boundary.
- `\B` represents a non-word boundary.

### Back-references
Back-references (`\1`, `\2`) refer to previously captured groups in the regex:
- `\1` refers back to the content matched by the first capturing group.

### Look-ahead and Look-behind
Look-ahead and look-behind assertions check for patterns without including them in the match:
- `(?=...)` is a positive look-ahead.
- `(?!...)` is a negative look-ahead.
- `(?<=...)` is a positive look-behind.
- `(?<!...)` is a negative look-behind.

## Author
My name is Spencer Klinkowize and I am a dedicated web development student passionate about demystifying complex programming concepts like regex. Check out more of my work on [GitHub](https://github.com/SpencerKlink).

# Regex Tutorial

Regex, which is short for regular expression, is a sequence of characters that defines a specific search patter. In this assignment I will be explaining what regex is by defining the individual parts of regex.

## Summary

In the tutorial, I will be explaning features of regex in a way that is understandible.

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
 Anchors are there for you to be able to define the search from the start or the end.

 In this case, /^ and $/ signify the beginning or end of the expression:

* The ^ matches the beginning of the string, or the beginning of a line if the multiline flag or (m) is enabled. This matches a position, not a character.
* The $ matches the end of the string, or the end of a line if the multiline flag (m) is enabled. This matches a position, not a character.
### Quantifiers
Quantifiers are there to tell you how many times a part of your expression should be repeated.

### OR Operator
|| is known as OR operator. The || acts like a boolean OR and it matches the expression before or after the ||. It can operate within a group, or on a whole expression. The patterns will be tested in order. It checks whether any of the two operands are non-zero (0, false, undefined, null or “” is considered as zero).

### Character Classes
Character classes match a character from a specific set. There are a number of predefined character classes but you can also define your own sets.

### Flags
Expression flags change how the expression is interpreted. Flags follow the closing forward slash of the expression. There are only 6 of them in JavaScript:

"i"
This flag ignore case so there is no difference between A or a.

"g" The (global) flag search retains the index of the last match, allowing subsequent searches to start from the end of
the previous match. Without the global flag, subsequent searches will return the same match.

"m" When the multiline flag is enabled, the beginning and end anchors (^ and $) will match the start and end of a line instead of the start and end of the whole string.

"u" The Unicode flag enables correct handling of surrogate pairs.

"s" The s enables the dotall . mode which will match any character, including newline.

### Grouping and Capturing
(ABC) () Regular expressions permit us to not just match text but also to extract information for further processing. This is done by defining groups of characters and capturing them using the special parentheses ( and ) metacharacters. Any sub pattern inside a pair of parentheses will be captured as a group. In practice, this can be used to extract information like phone numbers or emails from many types of data.

### Bracket Expressions
A bracket expression enclosed in square brackets is a regular expression that matches a single character, or ordered element. If the initial character is a circumflex ^, then this bracket expression is complemented.

### Greedy and Lazy Match
Greedy in regular expressions means matching the longest possible string. A greedy quantifier tells the engine to match as many instances of its quantified token or sub pattern as possible. This behavior is called greedy.

Lazy means matching the shortest possible string. A lazy quantifier tells the engine to match as few of the quantified tokens as needed. As you'll see in the table below, a regular quantifier is made lazy by appending a ? question mark to it.

### Boundaries
The \b is an anchor like the caret and the dollar sign. It matches at a position that is called a word boundary. This match is zero-length.

Characters that are matched by the short-hand character class \w are the characters that are treated as word characters by word boundaries.

Since digits are considered to be word characters, \b5\b can be used to match a 5 that is not part of a larger number. Putting a \b before and after an alphanumeric sequence matches are more exact than putting it “before and after a word”.

\B is the negated version of \b. \B matches at every location where \b does not. Effectively, \B matches at any position between two word characters as well as at any position between two non-word characters.

There are more boundaries with the regular expression. Some examples include POSIX, GNU and Tcl.

### Back-references
Backreferences match the same text as previously matched by a capturing group. Let’s say you want to match a pair of opening and closing HTML tags, and the text in between. By putting the opening tag into a backreference, we can reuse the name of the tag for the closing tag.

Here’s an example: <([A-Z][0-9]*)\b[^>]*>.*?</\1> This regular expression contains only one pair of parentheses, which capture the string matched by [A-Z][0-9]*. This is the opening HTML tag. The backreference \1 references the first capturing group. \1 matches the exact same text that was matched by the first capturing group. The / before it is a literal character. It is simply the forward slash in the closing HTML tag that we are trying to match.

### Look-ahead and Look-behind
Lookahead and lookbehind in a group are called “lookaround”, are zero-length declarations just like the start and end of line, and start and end of word anchors. There are positive and negative lookarounds.

## Author
Nathan Hogan currently attending a coding bootcamp at the University of Utah.

My Github: https://github.com/NathanHogan16

# Matching Email 

A regular expression is a type of object in Javascript used to check if a string contains a certain character or phrase. Here I will discuss Matching an Email Regex.

## Summary

Regular expressions are patterns used to match character combinations in strings. Simple patterns are constructed of characters for which you want to find a direct match. For example, the pattern /abc/ matches character combinations in strings only when the exact sequence "abc" occurs. 
When the search for a match requires something more than a direct match, such as finding one or more b's, or finding white space, you can include special characters in the pattern. 

The following example of a regular expression is "Matching a Email":


Matching an Email:

 /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.
([a-z\.]{2,6})$/

This pattern can be used as a basic email validation. It has different components as follows:


- [Anchors](#anchors)

- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

The regex is a a string of text and the pattern must be wrapped in a "/" for example:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ 

I am going tto break down each component for this example here:
### Anchors

The Matching an Email regex uses ^ and $ anchors. The ^ anchor is the begining of line that begins with a character. Anchor has two formats: 

- An exact string match. A regex is case sensitive, so this anchor would search for exact matches. fr instance ^ Horse would match "Horse" and "Horse Bridle", but not "horse" and "horse bridle". 

The $ anchor is the oposite of the previous anchor, which tells the regular expression to match the text before it at the end of the string. 

### Quantifiers

This regex uses the + which connects the email name, email provider, and the top level domain is for the email.

### Grouping Constructs

This regex has three groups seperated by the quantifier

([a-z0-9_.-]+)
([\da-z.-]+)
([a-z.]{2,6})

Together these form emailName@emailProvider.topLevelDomain

### Bracket Expressions

Putting a set of characters between square brackets makes that part of the expression match any of the characters between the brackets [a-z0-9_.-]. 

### Character Classes

This expression uses the character class \d. \d will match a single digit from 0-9. It also uses . to match any character except the new line character.
### The OR Operator

 abc|xyz is an example for the character "|" OR operator which matches abc or xyz.
### Flags

Outside the regular expression (at the end) flags helps with the pattern matching. For instance"

the letter i Ignore the case (uppercase and lowercase allowed).
the letter m Multi-line match.
the letter s Match new lines.
the letter x Allow spaces and comments.
the letter J Duplicate group names allowed.
the letter U Ungreedy match.

### Character Escapes

The \ in this expression escapes the character that would be searched for. In this example. - would not be searched for in the regex for the emailName.

## Author

THis was written by @WafaMohession

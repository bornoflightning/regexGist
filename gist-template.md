# Matching an Email with Regex

Here is an easy way to search and match an email using Regex, an explanation on how it works and how to apply it to your code.

## Summary

When searching through data, it is impossible to know what the exact input of the user will be. Regex allows you to search based on matching criteria for patters that fit the description of an email. The following snipped allows you to sift through endless literals using meta to find your search request.

<code>/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/</code>

## Table of Contents

- [Matching an Email with Regex](#matching-an-email-with-regex)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Grouping Constructs](#grouping-constructs)
    - [Bracket Expressions](#bracket-expressions)
    - [Character Classes](#character-classes)
    - [The OR Operator](#the-or-operator)
    - [Flags](#flags)
    - [Character Escapes](#character-escapes)
  - [Author](#author)

## Regex Components

Regex syntax is composed of a certain set of rules. The smalles unit of syntax is referred to as the atom, and it is a literal, or a literal character, literally. These literals are put together using () parenthesis to dictate rules about what atoms or literals to find. These meta characters dictate the type of character to find and the number of them in a row. Different symbols in our every day grammar have a specific use as rules to create metacharacters that help us locate data and literals. Below you will find an explanation of each.

### Anchors

Anchors are special sequences that help us match empty substrings. There are 3 and each one has a specific function
    1. ^ the carrot allows us to match a target string at the beginning of our search
    2. $ the money sign allows us to match the end of our target string
    3. \b the forward slash followed by the letter b allows us to set a specific boundary, such as matching the previous or the subsequent string. 

our Regex email search uses the '^' help us match a specified at the beginning of our string.

our code:
<code>/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/</code>

our example here uses an anchor at the end of our data.

### Quantifiers

Quantifiers help us control the quantity or number of a specific atom or literal we are trying to match. 
    1. * the star represents 0 or more
    2. + the plus sign helps us specify 1 or more ocurrenes of the atom
    3. ? the question mark help us specify either 0 or 1 occurence of the atom
    4. {n} curly braces allow us to specify a specific amount, or exaclty 'n'amount of occurences of the atom. 
    5. {m,n} when used with muyltiple values inside, it can help us specify a number of occurences between m and n.


quantifiers have the option of being followed by '?' which specify that the match be minimal instead of the maximum amount of matches


### Grouping Constructs

Below are our grouping protocols:

protocol : <code>([a-z0-9_\.-]+)</code>

subdomain & domain: <code>([\da-z\.-]+)</code>

domain extension: <code>"\.([a-z\.]{2,6})"</code>

path : no additional path provided

### Bracket Expressions

Bracket expressions represent a set of potential and allowed characters and are provided via a list of characters enclosed in brackets [].

    1. '^' The carrot matches any character that does NOT match the rest of the list
    2. '-' the minus sign at the beginnig means a literal.

here are some examples:

[br]at matches "bat" and "rat".
[^b]at matches all strings matched by .at except "bat".
[^hc]at matches all strings matched by .at other than "hat" and "cat".

our code:
<code>/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/</code>

our example here uses brackets to create an array requesting all alphabetical characters from a to z and all numerals from 0 to 9 in between the brackets [a-z0-9_\.-].

### Character Classes

Character classes allow us to distinguish between different types of characters. As an example, it can help us distinguish between numbers and letters. 
They are the most basic concept after the literal/atom. 

They can use parenthesis to specify all capital letters or lower case, and they can use \d to specify all digits

our code:
<code>/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/</code>

our code uses brackets to specify all lowercase letters


### The OR Operator

The or operator is used as pipe character '|'. It can be used to mix and match different combination of characters in a parenthesis, and will return any combination including the given input. As an exampe we can observe the word (pat). It is displayed as (p|a|t), but could also allow us to receive the input tap, or apt.

### Flags

Flags are referened with the letter g. This stands for global search and it allows us to search for all potential strings. The search is not case senstive.
Our code does not have any flags at the moment.

### Character Escapes

Escapes are special sequences that allow us to referenece the data as literal, meaning, it is not an input for a specified inquiry nor an atom, but rather a type of command. 
Here is a list of some common used commands which can be referenced with escape characters. Usually the capital letter used for that escape sequence refers to the NOT version of the sequence. 

    1. \w is used to specify a word
    2. \W is used to specify a NON-word character
    3. \d is used to specify a digit
    4. \D us used to specify a NON-digit

## Author

The author is Victor, an aspiring software engineer who would like to work for a fantastic company with flexible schedules and travel the world with his family. 
Github:
https://github.com/bornoflightning

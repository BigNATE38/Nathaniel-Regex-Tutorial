# Using Regex to Match an Email - Tutorial

The following tutorial shows how regex - Regular Expression - matches emails using the this expression: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. Node Inquirer or MongoDB can use regex to validate emails by making sure a user's email input contains a true match to the criteria given by the regex. 

## Summary

This tutorial will explain how regex - a series of characters that indicate a search pattern - validates an email. Instead of using literal characters, regex uses metacharacters which have more generalized fields of pattern. These broad criterias of pattern ultimately determine whether or not a user has created a valid email. 

## Table of Contents

- [Using Regex to Match an Email - Tutorial](#using-regex-to-match-an-email---tutorial)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Character Classes](#character-classes)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
    - [Greedy and Lazy Match](#greedy-and-lazy-match)
  - [Author](#author)

## Regex Components

### Anchors

The anchors , `^ ` `$` , mark the beginning and end of a string. On the other hand, the ```/ /``` before and after the anchors flags the start and end of the entire regex. The anchors themselves - `^ ` `$` - signify the actual search pattern within the back slashes. 

### Quantifiers

Quantifiers indicate the amount of characters in a given string. Both ```+```  symbols in this string are looking for 1 or more instances where the characters preciding it show up. 

The ```{}``` quantifier in this string has to be used in order to allow specifc numbers to be placed.

The ```()``` quantifier allows a sequence of characters to be grouped inside of it. In this case, a sequence of lower case letters, numbers, and snymbols can be grouped inside each of the parantheses to validate the email name, website, and top level domain - respectively. 

### Character Classes

The ```\d``` signifies a single digit ranging from 0 to 9. For example, it can only equal to a number such as "1", not "11". 

### Grouping and Capturing

There are three groups being captured in this string. The first group, ([a-z0-9_\.-]+), captures the email name. The next group, ([\da-z\.-]+), captures the name of the email service/site. Lastly, ([a-z\.]{2,6}), captures the top level domain - also know as - the .com.

### Bracket Expressions

The bracket expressions include [a-z0-9_\.-]. This means the validation looks for any lowercase letters anywhere from a-z. It also looks for any single numbers ranging from 0-9. It will also look for underscores or slashes in the email name. The \. allows a period to be in the email name. However, if a forward slash was missing the period would mean it searches for any character preceding it. The [\da-z\.-] means the email service looks for any number 0-9, lower case letters a-z, periods or dashes. The top level domain's bracket expression, [a-z\.], looks for lowercase letters or a period. 

### Greedy and Lazy Match

As stated, the ```{}``` quantifier in this string has to be used in order to allow specifc numbers to be placed. In this case, the greedy match allows the email's top-level domain to be validated anywhere between 2 and 6 characters. 

## Author

Created by Nathaniel Vanderpoort. For any further questions, please visit [GitHub profile](https://github.com/BigNATE38).

# Regex Tutorial: Matching an Email

 A regular expression or regex is very useful for search patterns that make it more convenient for programmers to define a specific set of rules that they may use on several different occasions. For this regex tutorial, we will be looking at the regex for matching an email. This regex is typically used with technologies like MongoDB and Node's Inquirer to validate emails. 

## Summary

``` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ ```

 This regex has many different components to ensure that the email matches. In this tutorial, I will be going over the different components that are standard to a regex and other components that allow for this regex in particular to be succesful, such as anchors, quantifiers, grouping constructs and a couple of others. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)
- [Closing](#closing)
- [Author](#author)
- [Resource](#resources)

## Regex Components

 One of the most standard components to a regex are the slash characters (/). Because a regex, in this case, is in literal notation, we need them at the beginning and end of a regex. Another important thing to note about a regex is that they are case-sensitive. 

### Anchors

- In between the slash characters are two symbols known as anchors, ^ and $. The ^ anchor let's us know that the string should begin with the charcters that follow. In this case, the ^ anchor is followed by [bracket expressions](#bracket-expressions).

- At the end of the regex before the slash is another anchor, $, which implies what the ending of the regex should include.

### Quantifiers

- Quantifiers give us a range of characters that our email should be between. They appear in curly brackets as such {2,6}. 2 would be the minimum number and 6 the maximum number that the regex should look for in our last [subexpression](#grouping-constructs).

- Quantifiers can be greedy or lazy by adding the respective symbols after it, *, ?. 

- Another quantifier in this expression is the (+) which combines the parts of the email together. So, in this case, the users email name, the email provider and ".com" will all be added together. 

### Grouping Constructs

- Grouping constructs help us know how are regex is broken up. They are parenthesis that are also referred to as subexpressions. 
Our regex has three subexpressions.

```([a-z0-9_\.-]+)```       ```([\da-z\.-]+)```       ```([a-z\.]{2,6})```


### Bracket Expressions

- Bracket expressions or positive character groups, imply that a range of charcters are accepted. In this case, all charcters "a" through "z", "0" through "9", and the characters "_\.-" are accepted. 
- Bracket expressions can be turned into negative character roups by add a "^" to the beginning of the expression. 

- The hyphen between the letter and the numbers signify the range of the letters and numbers.

### Character Classes

- The character class \d in this case will match one character from numeral digit. It is equivalent to [0-9].

### Character Escapes

- The back slash (\) in a regex is a character escape, which signifies a charcter that is not to be taken literally. A period in a regex would match any character except the newline character (/n) but in this case "\." it just means to look for a period. 

### Closing

- In the end, our email should have any characters a-z, 0-9, or "_\.-" plus an "@" symbol followed by an email provider which includes the characters 0-9 and a-z, "\.-"  and a period followed by any characters a-z that are between 2 and 6 characters long. 

## Author

Reagin Turner is a software developer currently in Atlanta, Georgia. Please visit her [github profile here](https://github.com/Reagintaylor).

## Resources

- [Regex Tutorial](https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial)
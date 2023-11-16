# Matching a URL - Regex Tutorial

This ReadME document provides a detailed explanation of the URL matching regular expression (regex).

## Summary

  This regex is used to identify and validate URLs. Including the verification of the protocol, domain, and path. It offers flexibility by accommodating URLs with or without a specified protocol (http or https).

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
The regex makes use of "^" and "$" anchors to ensure that the entire string is matched, validating the URL from start to finish.

### Quantifiers
The question mark (?) following (https?:\/\/) indicates that this section is optional, allowing URLs to be validated with or without a specified protocol (http or https). 
For example, the URL can have "http://" or "https://" or in some cases not at all.

### Grouping Constructs
- (https?:\/\/)?: This part matches the protocol (http or https) and is optional.

- ([\da-z\.-]+): This part captures the domain name. It allows for alphanumeric characters, dots, and hyphens.

- \.([a-z\.]{2,6}): This captures the top-level domain (TLD). (ex: ".com", ".org", etc.)

- ([\/\w \.-]*)*: This part captures the path, which can be a mix of letters, numbers, slashes, spaces, dots, and hyphens.

- \/?$: This makes sure that the path ends with a slash if it's there, but is also optional.

### Bracket Expressions
[\da-z\.-]: This expression matches alphanumeric characters, dots, and hyphens in the domain name.

### Character Classes
\d: This matches numbers.
\w: This matches word characters (alphanumeric + underscore).

### The OR Operator
https?: The ? makes the 's' in 'https' optional, allowing for both http and https.

### Flags
No flags are used in this regex.

### Character Escapes
No special characters need to be escaped in this check.

## Author

Jake Preciado

GitHub: https://github.com/jmpre28
Email: jacobpreciado@gmail.com


# J Lang Design

J Lang is designed with 3 key principals:

1. **Enforced Security**: J Lang is designed to enforce security. All variables are homorphically encrypted at all times. It is **not falsey**, and it will make no assumptions about types or traits that are not directly written.

2. **Extensible**: J Lang is made to interact with other packages and languages. Everything in J Lang is extensible, allowing easy additions to packages and adding scalability to programs.

3. **IDE Optimization**: J Lang is designed to be written in an IDE. J Lang syntax is designed to work well with autocomplete in order to allow both readability and agility in development.

### Table of Contents

1. [Variable Declarations](https://github.com/theswerd/j/tree/main/docs/design/variable-declarations.md)


## Other
- Minimal use of caps - only using them for areas that are meant to be used in small amounts 
- Language is kebab-case
- Spaces are a part of syntax: g- is different than g -
- variable names cannot end with -
- prefers single quote, allows double quote in formating with single quote is used in string
- imports should be java styled + dart show/hide/as as they are not strings to be manipulated they are paths
- multiline strings with `
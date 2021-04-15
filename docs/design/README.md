# J Lang Design

J Lang is designed with 3 key principals:

1. **Enforced Security**: J Lang is designed to enforce security. All variables are homorphically encrypted at all times. It is **not falsey**, and it will make no assumptions about types or traits that are not directly written.

2. **Extensible**: J Lang is made to interact with other packages and languages. Everything in J Lang is extensible, allowing easy additions to packages and adding scalability to programs.

3. **IDE Optimization**: J Lang is designed to be written in an IDE. J Lang syntax is designed to work well with autocomplete in order to allow both readability and agility in development.

### Syntax Notes

#### Variable Declarations

##### Structure

```
type name: trait1, trait2 = value
```


##### Examples

Primitives:
```
int age = 20; // mutable by default
final string name = 'jlang';
```

Types and Traits
```
// Type definition
type person {
    string first-name,
    string? middle-initial, // nullable
    string last-name,
    int age = 0 // default
}

type book {
    string name,
    string summary
}

// Traits
trait summary {
    string summary; // Can be getter or string
}

extend person with summary {
   string summary => first-name + ' ' + middle-initial + ' ' + last-name
}



person president = (
    first-name = 'Joe',
    middle-initial = 'R',
    last-name = 'Biden'
);


let vice-president: summary = person(
    first-name = 'Kamala',
    middle-initial = 'D',
    last-name = 'Harris'
);

let great-book: summary = book(
    name = "Cryptonomicon",
    summary = 'The "cryptographer\'s bible"'
);
```


#### Other
- Minimal use of caps - only using them for areas that are meant to be used in small amounts 
- Language is kebab-case
- Spaces are a part of syntax: g- is different than g -
- variable names cannot end with -
- prefers single quote, allows double quote in formating with single quote is used in string

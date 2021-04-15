## Variable Declarations

### Structure

**Overall**:
```
type name: trait1, trait2 = value
```
**Primitives** 
```
let my-string = 'string'
```
**Set Type**
```
event my-type = (
    location = 'Los Angeles',
    description = 'J Lang Convention'
)
```
**Trait**
```
let summarizable-type: summary = MySummarizableType(
    name = 'type name',
    description = 'description of whatever this is'
)
```

### Examples

Primitives:
```
int age = 20 // mutable by default
final string name = 'jlang'
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
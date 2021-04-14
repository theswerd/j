# J Lang Design

J Lang is designed with 3 key principals:

1. **Enforced Security**: J Lang is designed to enforce security. All variables are homorphically encrypted at all times. It is **not falsey**, and it will make no assumptions about types or traits that are not directly written.

2. **Extensible**: J Lang is made to interact with other packages and languages. Everything in J Lang is extensible, allowing easy additions to packages and adding scalability to programs.

3. **IDE Optimization**: J Lang is designed to be written in an IDE. J Lang syntax is designed to work well with autocomplete in order to allow both readability and agility in development.


### Variable Declarations

```j
string name = 'jlang'

int born = 2021

float bens-height-in-meters = 1.778


// Struct is not for sure yet
struct user{
    string name,
    string bio,
    int followers
}

extend user {
    user new-user (string name, {string biography = ''}) => {
        followers = 0,
        name,
        bio: biography
    }
}

user my-user = {
    name = 'jlang',
    bio = 'new encrypted language',
    followers = 15
}

user my-user-2 = .new-user('jlang', biography: 'a super cool language')
```

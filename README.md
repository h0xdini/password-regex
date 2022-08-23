# password-regex

Minimum eight characters, at least one letter and one number:
```js
^(?=.*[A-Za-z])(?=.*\d)[A-Za-z\d]{8,}$
```

Minimum eight characters, at least one letter, one number and one special character:
```js
^(?=.*[A-Za-z])(?=.*\d)(?=.*[@$!%*#?&])[A-Za-z\d@$!%*#?&]{8,}$
```

Minimum eight characters, at least one uppercase letter, one lowercase letter and one number:
```js
^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)[a-zA-Z\d]{8,}$
```

Minimum eight characters, at least one uppercase letter, one lowercase letter, one number and one special character:
```js
^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$
```

Minimum eight and maximum 10 characters, at least one uppercase letter, one lowercase letter, one number and one special character:
```js
^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,10}$
```

---------------------------------------------------------------
Minimumu eight characters, at least one uppercase letter, one lowercase letter, one special character, numbers are not crutial
```js
^(?=.*[a-z])(?=.*[A-Z])(?=.*[@$#!%*?&])[A-Za-z0-9@#$!%*?&]{8,}$
```
---------------------------------------------------------------
## Detailed
```js
(?=.*[a-z])        // use positive look ahead to see if at least one lower case letter exists
(?=.*[A-Z])        // use positive look ahead to see if at least one upper case letter exists
(?=.*\d)           // use positive look ahead to see if at least one digit exists
[-+_!@#$%^&*.,?]   // use positive look ahead to see if at least one non-word character exists
```

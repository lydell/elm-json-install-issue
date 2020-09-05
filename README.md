# elm-json install issue

1. Clone this repo.

2. `npm ci`

   Expected: Everything is installed.
   Actual: The postinstall hook for `elm-json` fails somehow.

3. `npm i`. Everything works.

4. Remove postinstall script in package.json of this repo. Now `npm ci` works.

Update: A workaround is to add this to your package.json:

```
"name": "whatever"
```

https://stackoverflow.com/questions/59777226/npm-ci-throws-exception-cannot-read-property-length-of-undefined

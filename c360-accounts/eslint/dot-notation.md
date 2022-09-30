
Without the rule **"@typescript-eslint/dot-notation": "off"** when we run ```npm run lint:fix```
the following happens
```ts
// before running "npm run lint:fix"
let policyWithDetails = {}
policyWithDetails['id'] = 'de3221dd' // this does not throw an error 
// after running "npm run lint:fix"
let policyWithDetails = {}
policyWithDetails.id = 'de3221dd' // this throws Typescript error property id does not exist on Object type
```
To avoid these kind of errors we need to use the **"@typescript-eslint/dot-notation": "off"** rule
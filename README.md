### Is this a bug report?

yes

### Steps to Reproduce

1. create app `npx create-react-app app`
2. replace content of `src/App.js` with
```javascript
import React from 'react';

const App = (
  <>App</>
);

export default App;
```
3. run `npx eslint ./src` inside `app`


### Expected Behavior

no errors, no warnings

### Actual Behavior

There is a warning:
```
.../src/App.js
  1:8  warning  'React' is defined but never used  no-unused-vars

✖ 1 problem (0 errors, 1 warning)
```
If I remove react import from `src/App.js`, then it shows an error:
```
.../src/App.js
  2:3  error  'React' must be in scope when using JSX  react/react-in-jsx-scope

✖ 1 problem (1 error, 0 warnings)
```

### Reproducible Demo

https://github.com/vadzim/errorneous-fragment-linting.git


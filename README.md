<!--
  PLEASE READ THE FIRST SECTION :-)
-->

### Is this a bug report?

yes

<!--
  If you answered "Yes":
  
    Please note that your issue will be fixed much faster if you spend about
    half an hour preparing it, including the exact reproduction steps and a demo.
    
    If you're in a hurry or don't feel confident, it's fine to report bugs with
    less details, but this makes it less likely they'll get fixed soon.

    In either case, please fill as many fields below as you can.

  If you answered "No":

    If this is a question or a discussion, you may delete this template and write in a free form.
    Note that we don't provide help for webpack questions after ejecting.
    You can find webpack docs at https://webpack.js.org/.
-->


### Steps to Reproduce

<!--
  How would you describe your issue to someone who doesn’t know you or your project?
  Try to write a sequence of steps that anybody can repeat to see the issue.
-->

(Write your steps here:)

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

<!--
  How did you expect the tool to behave?
  It’s fine if you’re not sure your understanding is correct.
  Just write down what you thought would happen.
-->

no errors, no warnings


### Actual Behavior

<!--
  Did something go wrong?
  Is something broken, or not behaving as you expected?
  Please attach screenshots if possible! They are extremely helpful for diagnosing issues.
-->

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

<!--
  If you can, please share a project that reproduces the issue.
  This is the single most effective way to get an issue fixed soon.

  There are two ways to do it:

    * Create a new app and try to reproduce the issue in it.
      This is useful if you roughly know where the problem is, or can’t share the real code.

    * Or, copy your app and remove things until you’re left with the minimal reproducible demo.
      This is useful for finding the root cause. You may then optionally create a new project.

  This is a good guide to creating bug demos: https://stackoverflow.com/help/mcve
  Once you’re done, push the project to GitHub and paste the link to it below:
-->

https://github.com/vadzim/errorneous-fragment-linting.git


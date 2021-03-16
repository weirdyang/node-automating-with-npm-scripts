
1. Add script to analyse the source code and report lint errors
   Open package.json and go to the scripts section. Add a new key named lint with the value npx standard \"src/*.js\".

2. Create script to automatically fix and format code that's not following the style guide
   Add another key named lint-fix with value npx standard \"src/*.js\" --fix as the value.
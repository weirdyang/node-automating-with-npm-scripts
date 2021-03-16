
1. Add a start script to build and run the application
   Open package.json and go to the scripts section. Add a new key named start and set the value to npm run build && node build/index.js

2. Add script to run the application in development mode
   Add a key named start-dev to the scripts object and give it the value nodemon --watch src --exec PORT=5000 npm start.
   This script uses nodemon to watch for file changes and each time the code changes, it'll execute the npm start script.

3. Add pre hook for the start-dev script
   We want to run the linter and fix errors before running the start-dev script and we will use pre hook for the script to achieve this.
   Add a new key named prestart-dev with a value of npm run lint-fix to the scripts object.
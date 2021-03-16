1. Create script that will transpile the code using Babel
   Open package.json and go to the scripts section. Add a script named build with the value babel src -d build to transpile the source code using Babel.

2. Add a script to clean up the build directory
   There will be situations you'll need to cleanup the build directory. For that reason, add a script named build-clean to the scripts object and put rm -rf build as the value for that key.

3. Add post hook for the build-clean script
   Add post hook for the build-clean script by adding a new key named postbuild-clean with a value of npm run build.
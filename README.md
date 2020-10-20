# Demo of problem when there is a whitespace in a tartufo excludes file
To replicate:
1. Clone this repo
2. Navigate into the root directory
3. Run `tartufo -x .tartufo-no-whitespace-excludes scan-local-repo .`. It will report potential problems with `src/shouldAlsoFail.js`
4. Run `tartufo -x .tartufo-with-whitespace-excludes scan-local-repo .`. It will not report the potential problems

The `.tartufo-no-whitespace-excludes` file contains a line return which seems to cause `Tartufo` fail to find any problems

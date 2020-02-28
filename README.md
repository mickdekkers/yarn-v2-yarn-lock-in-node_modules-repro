## Steps to reproduce

1. Just run `yarn`

## Output

```
$ yarn
➤ YN0000: ┌ Resolution step
➤ YN0032: │ fsevents@npm:1.2.11: Implicit dependencies on node-gyp are discouraged
➤ YN0032: │ nan@npm:2.14.0: Implicit dependencies on node-gyp are discouraged
➤ YN0000: └ Completed in 5.35s
➤ YN0000: ┌ Fetch step
➤ YN0000: └ Completed in 2.11s
➤ YN0000: ┌ Link step
➤ YN0007: │ parse-domain@npm:2.3.4 must be built because it never did before or the last one failed
➤ YN0009: │ parse-domain@npm:2.3.4 couldn't be built successfully (exit code 1, logs can be found here: /var/folders/8x/fhhgsgvj68g7knzw6lg9sjsm0000gp/T/logfile-9693Xl6iUlpP7Dz9.log)
➤ YN0000: └ Completed in 9.61s
➤ YN0000: Failed with errors in 17.11s
```


## Error log

```
# This file contains the result of Yarn building a package (parse-domain@npm:2.3.4)
# Script name: postinstall

Usage Error: The nearest package directory (/repro/yarn-v2-yarn-lock-in-node_modules/node_modules/parse-domain) doesn't seem to be part of the project declared at /repro/yarn-v2-yarn-lock-in-node_modules. If the project directory is right, it might be that you forgot to list a workspace. If it isn't, it's likely because you have a yarn.lock file at the detected location, confusing the project detection.

$ yarn run <scriptName> ...
ERROR: "build:tries" exited with 1.

```

## Version info

```sh
$ yarn -v
2.0.0-rc.29
$ node -v
v12.13.1
```

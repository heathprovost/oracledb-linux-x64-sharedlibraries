# oracledb-linux-x64-sharedlibraries

This module exists to simply unzip and make available the shared libaries needed 
by [node oracledb](https://github.com/oracle/node-oracledb) for Linux x64 in order
to successfully run the oracledb client locally.

This module should always be included as a dev dependency and there is no need 
to ever import or require it, it does everything it needs to do during npm 
post-install. It is the responsibility of the user to ensure that their LD_LIBRARY_PATH 
is updated to include this modules ./lib folder, otherwise this module does nothing 
useful at all. This can be accomplished for a VS Code project by adding this to
your `.vscode/settings.json` file:

```
"terminal.integrated.env.linux": {
  "LD_LIBRARY_PATH": "${workspaceFolder}/node_modules/@heathprovost/oracledb-linux-x64-sharedlibraries/lib"
}
```

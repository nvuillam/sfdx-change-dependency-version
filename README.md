sfdx-change-dependency-version
==============================

Allows to change the external packages dependencies versions in local sfdx project files files

[![Version](https://img.shields.io/npm/v/sfdx-change-dependency-version.svg)](https://npmjs.org/package/sfdx-change-dependency-version)
[![CircleCI](https://circleci.com/gh/nvuillam/sfdx-change-dependency-version/tree/master.svg?style=shield)](https://circleci.com/gh/nvuillam/sfdx-change-dependency-version/tree/master)
[![Appveyor CI](https://ci.appveyor.com/api/projects/status/github/nvuillam/sfdx-change-dependency-version?branch=master&svg=true)](https://ci.appveyor.com/project/heroku/sfdx-change-dependency-version/branch/master)
[![Codecov](https://codecov.io/gh/nvuillam/sfdx-change-dependency-version/branch/master/graph/badge.svg)](https://codecov.io/gh/nvuillam/sfdx-change-dependency-version)
[![Greenkeeper](https://badges.greenkeeper.io/nvuillam/sfdx-change-dependency-version.svg)](https://greenkeeper.io/)
[![Known Vulnerabilities](https://snyk.io/test/github/nvuillam/sfdx-change-dependency-version/badge.svg)](https://snyk.io/test/github/nvuillam/sfdx-change-dependency-version)
[![Downloads/week](https://img.shields.io/npm/dw/sfdx-change-dependency-version.svg)](https://npmjs.org/package/sfdx-change-dependency-version)
[![License](https://img.shields.io/npm/l/sfdx-change-dependency-version.svg)](https://github.com/nvuillam/sfdx-change-dependency-version/blob/master/package.json)

<!-- toc -->
* [Debugging your plugin](#debugging-your-plugin)
<!-- tocstop -->
<!-- install -->
<!-- usage -->
```sh-session
$ npm install -g sfdx-change-dependency-version
$ sfdx-change-dependency-version COMMAND
running command...
$ sfdx-change-dependency-version (-v|--version|version)
sfdx-change-dependency-version/0.0.0 win32-x64 node-v8.9.4
$ sfdx-change-dependency-version --help [COMMAND]
USAGE
  $ sfdx-change-dependency-version COMMAND
...
```
<!-- usagestop -->
<!-- commands -->
* [`sfdx-change-dependency-version change-dependency:execute`](#sfdx-change-dependency-version-change-dependencyexecute)

## `sfdx-change-dependency-version change-dependency:execute`

Allows to change an external package dependency version

```
USAGE
  $ sfdx-change-dependency-version change-dependency:execute

OPTIONS
  -f, --folder=folder              SFDX project folder containing files
  -j, --majorversion=majorversion  Major version
  -m, --minorversion=minorversion  Minor version
  -n, --namespace=namespace        Namespace of the managed package

DESCRIPTION


EXAMPLE
  $ sfdx change-dependency:execute -n FinServ -j 214 -m 7
```

_See code: [src/commands/change-dependency/execute.ts](https://github.com/nvuillam/sfdx-change-dependency-version/blob/v0.0.0/src/commands/change-dependency/execute.ts)_
<!-- commandsstop -->
<!-- debugging-your-plugin -->
# Debugging your plugin
We recommend using the Visual Studio Code (VS Code) IDE for your plugin development. Included in the `.vscode` directory of this plugin is a `launch.json` config file, which allows you to attach a debugger to the node process when running your commands.

To debug the `hello:org` command: 
1. Start the inspector
  
If you linked your plugin to the sfdx cli, call your command with the `dev-suspend` switch: 
```sh-session
$ sfdx hello:org -u myOrg@example.com --dev-suspend
```
  
Alternatively, to call your command using the `bin/run` script, set the `NODE_OPTIONS` environment variable to `--inspect-brk` when starting the debugger:
```sh-session
$ NODE_OPTIONS=--inspect-brk bin/run hello:org -u myOrg@example.com
```

2. Set some breakpoints in your command code
3. Click on the Debug icon in the Activity Bar on the side of VS Code to open up the Debug view.
4. In the upper left hand corner of VS Code, verify that the "Attach to Remote" launch configuration has been chosen.
5. Hit the green play button to the left of the "Attach to Remote" launch configuration window. The debugger should now be suspended on the first line of the program. 
6. Hit the green play button at the top middle of VS Code (this play button will be to the right of the play button that you clicked in step #5).
<br><img src=".images/vscodeScreenshot.png" width="480" height="278"><br>
Congrats, you are debugging!

sfdx-change-dependency-version
==============================

Allows to change the external packages dependencies versions in local sfdx project files files

[![Version](https://img.shields.io/npm/v/sfdx-change-dependency-version.svg)](https://npmjs.org/package/sfdx-change-dependency-version)
[![Downloads/week](https://img.shields.io/npm/dw/sfdx-change-dependency-version.svg)](https://npmjs.org/package/sfdx-change-dependency-version)
[![License](https://img.shields.io/npm/l/sfdx-change-dependency-version.svg)](https://github.com/nvuillam/sfdx-change-dependency-version/blob/master/package.json)

# INSTALLATION

```
    sfdx plugins:install sfdx-change-dependency-version
```

- Windows users: [sfdx plugin generator](https://github.com/forcedotcom/sfdx-plugin-generate) is bugged on windows (hardcode call of linux rm instruction) , so you may use [Git Bash](https://gitforwindows.org/) to run this code ( at least while it installs the plugin dependencies )

## `change-dependency:execute`

Allows to change an external package dependency version

```
USAGE
  $ change-dependency:execute OPTIONS

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

oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g mynewplugin
$ mynewplugin COMMAND
running command...
$ mynewplugin (--version)
mynewplugin/0.0.0 darwin-arm64 node-v16.18.0
$ mynewplugin --help [COMMAND]
USAGE
  $ mynewplugin COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`mynewplugin hello PERSON`](#mynewplugin-hello-person)
* [`mynewplugin hello world`](#mynewplugin-hello-world)
* [`mynewplugin help [COMMAND]`](#mynewplugin-help-command)
* [`mynewplugin plugins`](#mynewplugin-plugins)
* [`mynewplugin plugins:install PLUGIN...`](#mynewplugin-pluginsinstall-plugin)
* [`mynewplugin plugins:inspect PLUGIN...`](#mynewplugin-pluginsinspect-plugin)
* [`mynewplugin plugins:install PLUGIN...`](#mynewplugin-pluginsinstall-plugin-1)
* [`mynewplugin plugins:link PLUGIN`](#mynewplugin-pluginslink-plugin)
* [`mynewplugin plugins:uninstall PLUGIN...`](#mynewplugin-pluginsuninstall-plugin)
* [`mynewplugin plugins:uninstall PLUGIN...`](#mynewplugin-pluginsuninstall-plugin-1)
* [`mynewplugin plugins:uninstall PLUGIN...`](#mynewplugin-pluginsuninstall-plugin-2)
* [`mynewplugin plugins update`](#mynewplugin-plugins-update)

## `mynewplugin hello PERSON`

Say hello

```
USAGE
  $ mynewplugin hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/rhumbertgz/mynewplugin/blob/v0.0.0/dist/commands/hello/index.ts)_

## `mynewplugin hello world`

Say hello world

```
USAGE
  $ mynewplugin hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ mynewplugin hello world
  hello world! (./src/commands/hello/world.ts)
```

## `mynewplugin help [COMMAND]`

Display help for mynewplugin.

```
USAGE
  $ mynewplugin help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for mynewplugin.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.16/src/commands/help.ts)_

## `mynewplugin plugins`

List installed plugins.

```
USAGE
  $ mynewplugin plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ mynewplugin plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.1.5/src/commands/plugins/index.ts)_

## `mynewplugin plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ mynewplugin plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ mynewplugin plugins add

EXAMPLES
  $ mynewplugin plugins:install myplugin 

  $ mynewplugin plugins:install https://github.com/someuser/someplugin

  $ mynewplugin plugins:install someuser/someplugin
```

## `mynewplugin plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ mynewplugin plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ mynewplugin plugins:inspect myplugin
```

## `mynewplugin plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ mynewplugin plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ mynewplugin plugins add

EXAMPLES
  $ mynewplugin plugins:install myplugin 

  $ mynewplugin plugins:install https://github.com/someuser/someplugin

  $ mynewplugin plugins:install someuser/someplugin
```

## `mynewplugin plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ mynewplugin plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ mynewplugin plugins:link myplugin
```

## `mynewplugin plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ mynewplugin plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ mynewplugin plugins unlink
  $ mynewplugin plugins remove
```

## `mynewplugin plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ mynewplugin plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ mynewplugin plugins unlink
  $ mynewplugin plugins remove
```

## `mynewplugin plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ mynewplugin plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ mynewplugin plugins unlink
  $ mynewplugin plugins remove
```

## `mynewplugin plugins update`

Update installed plugins.

```
USAGE
  $ mynewplugin plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->

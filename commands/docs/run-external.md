---
title: run-external
categories: |
  system
version: 0.86.0
system: |
  Runs external command.
usage: |
  Runs external command.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for system

<div class='command-title'>{{ $frontmatter.system }}</div>

## Signature

```> run-external {flags} (command) ...rest```

## Flags

 -  `--redirect-stdout, -`: redirect stdout to the pipeline
 -  `--redirect-stderr, -`: redirect stderr to the pipeline
 -  `--redirect-combine, -`: redirect both stdout and stderr combined to the pipeline (collected in stdout)
 -  `--trim-end-newline, -`: trimming end newlines

## Parameters

 -  `command`: external command to run
 -  `...rest`: arguments for external command


## Input/output types:

| input | output |
| ----- | ------ |
| any   | any    |

## Examples

Run an external command
```nu
> run-external "echo" "-n" "hello"

```

Redirect stdout from an external command into the pipeline
```nu
> run-external --redirect-stdout "echo" "-n" "hello" | split chars

```

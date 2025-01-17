# affected:lint

Lint projects affected by changes

## Usage

```bash
nx affected:lint
```

Install `@nrwl/cli` globally to invoke the command directly using `nx`, or use `npm run nx` or `yarn nx`.

### Examples

Run lint in parallel:

```bash
nx affected:lint --parallel --maxParallel=5
```

Rerun the lint target only for the projects that failed last time:

```bash
nx affected:lint --only-failed
```

Run the lint target for all projects:

```bash
nx affected:lint --all
```

Run lint for all the projects affected by changing the index.ts file:

```bash
nx affected:lint --files=libs/mylib/src/index.ts
```

Run lint for all the projects affected by the changes between master and HEAD (e.g., PR):

```bash
nx affected:lint --base=master --head=HEAD
```

Run lint for all the projects affected by the last commit on master:

```bash
nx affected:lint --base=master~1 --head=master
```

## Options

### all

All projects

### base

Base of the current branch (usually master)

### exclude

Default: ``

Exclude certain projects from being processed

### files

Change the way Nx is calculating the affected command by providing directly changed files, list of files delimited by commas

### head

Latest commit of the current branch (usually HEAD)

### help

Show help

### maxParallel

Default: `3`

Max number of parallel processes

### only-failed

Default: `false`

Isolate projects which previously failed

### parallel

Default: `false`

Parallelize the command

### plain

Produces a plain output for affected:apps and affected:libs

### uncommitted

Uncommitted changes

### untracked

Untracked changes

### verbose

Print additional error stack trace on failure

### version

Show version number

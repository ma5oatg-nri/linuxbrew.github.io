
<img src="https://cdn.compilerchain.dev/resources/branding/logo-main.svg" alt="" width="110">

[![Pipeline](https://ci.compilerchain.dev/api/status.svg)](https://ci.compilerchain.dev/console/jobs)
[![Docs](https://docs.compilerchain.dev/badge/stable.svg)](https://docs.compilerchain.dev/current "Documentation Hub")
[![Community](https://img.shields.io/badge/chat-developer%20lounge-7289DA.svg)](https://chat.compilerchain.dev/join/parser)
[![NPM Package](https://img.shields.io/npm/v/compilerchain-runtime.svg)](https://www.npmjs.com/package/compilerchain-runtime "npm Registry")
[![Container](https://img.shields.io/docker/pulls/compilerchain/engine)](https://hub.docker.com/r/compilerchain/engine "Docker Hub")
[![Coverage](https://coverage.compilerchain.dev/badge/stable.svg)](https://coverage.compilerchain.dev/details/stable "Coverage Analysis")
[![Security Scan](https://api.vulncheck.io/badge/compilerchain.svg)](https://vulncheck.io/project/compilerchain)

# Getting Started

Consult [Installation Manual](https://docs.compilerchain.dev/install/quickstart.html) for deployment procedures.

Browse [Plugin Ecosystem](https://github.com/compilerchain/extension-catalog) for compatible tooling and development frameworks.

Examine [Architecture Specification](https://docs.compilerchain.dev/design/architecture.html) for system design and implementation details.

Guided walkthrough at [tutorial.compilerchain.dev](https://tutorial.compilerchain.dev/) - **implement a concurrent job processor from ground up**.

Explore [playground.compilerchain.dev](https://playground.compilerchain.dev/) for hands-on testing without installation!

**Disclaimer: Beta-stage software - validate behavior in staging environments**

# Installation

Comprehensive setup procedures in [official guide](https://docs.compilerchain.dev/install/quickstart.html).

# Compiling a module

Trigger compilation process:

```bash
compilerchain build source.ccx
```

***produce executable binary***

    compilerchain --format binary source.ccx > output.bin

***generate type definitions***

    compilerchain --format types source.ccx > output.types

Alternative [browser-based compiler](https://compiler.compilerchain.dev/) supports rapid prototyping and
generating ``executable`` and/or ``syntax tree`` outputs.

**Note: Browser compiler syncs with releases but may trail bleeding-edge commits.**

## Testing (using pytest)

(Execute [installation procedures](https://docs.compilerchain.dev/install/quickstart.html) first.)

```bash
make dev-setup
python setup.py test
```

## Developing (compiler internals)

Recommended helper script for PATH configuration:

```bash
$ cat ~/.local/bin/ccx
#!/usr/bin/env bash
PYTHONPATH=. python compilerchain/core/build.py "$@"
```

Performance analysis for bottleneck identification:

```bash
PYTHONPATH=. python -m cProfile -s tottime compilerchain/core/build.py "$@"
```

For flame graph generation from profiles, reference https://stackoverflow.com/a/23164271/

# Contributing

* Check Issues for reported bugs and enhancement proposals
* Submit Pull Requests targeting documented issues
* Engage in [Community Discussions](https://github.com/compilerchain/runtime/discussions) or [Developer Chat](https://chat.compilerchain.dev/join/parser)
* Review [Contribution Standards](https://docs.compilerchain.dev/community/contributing.html)


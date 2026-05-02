# felix

let felix fix it — automated Java dependency upgrades for Maven and Gradle.

## Install

```sh
brew install alchemain/taps/felix
```

This taps `alchemain/homebrew-taps` and installs the `felix` binary to your Homebrew prefix.

## Quickstart

Run from a directory with a `pom.xml` or `build.gradle`:

```sh
felix login                            # browser-based auth with Alchemain
felix scan                             # find vulnerable / outdated deps
felix deps:update <group:artifact>     # apply an upgrade
felix deps:graph                       # show the resolved dep graph
```

Use `-r <path>` to target a project in a different directory.

## Bring your own Anthropic key

By default, felix runs on the Alchemain free tier. If you'd rather use your own Anthropic key:

```sh
export ANTHROPIC_API_KEY=sk-ant-...
felix deps:update <group:artifact>
```

You'll be prompted once to confirm; the choice is remembered locally.

## Update

```sh
brew upgrade felix
```

## Help

```sh
felix --help
felix <command> --help
```

---

This repository hosts release artifacts for the `felix` CLI distributed via Homebrew. Source is private. File issues at https://github.com/alchemain/felix/issues.

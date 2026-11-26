# AGENTS.md

`lus-lang/atmos-yaml` is the repository of the `yaml` package of the atmosphere registry. Programs load the package with `require("https://atmosp.here/2.0/yaml.lus")`.

## Scope

`yaml` reads and writes YAML 1.2 with the core schema. The public API is every function that `yaml.lus` returns in its module table. A change to that API needs a new entry in `CHANGELOG.md` and a version change in the header.

## Layout

- `yaml.lus` is the whole package. Its header doc comment contains the package metadata and the declared permissions.
- `tests/*_test.lus` are the tests. They load `yaml.lus` from the parent of `TEST_DIR`, the directory that holds the test file.

## Commands

Run these commands from the root of the repository.

```sh
lus test tests          # run the tests
lus check yaml.lus     # lint, including the package codes
lus doc yaml.lus       # print the reference
```

## Rules

- Every public function has a doc comment that states each result and each error, following `spec/design/style.md` of the Lus repository.
- The package never calls `pledge`. A new permission is declared in the header.
- Prose follows the `lus-writing` skill, which `lus agents init` installs and https://lus.dev/agents/skills/lus-writing/SKILL.md serves. In particular, prose has no dashes or semicolons and never names the Roblox Lua dialect.
- Every bug fix comes with a test that fails without it.

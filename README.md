# yaml

Reads and writes YAML 1.2 with the core schema.

```lus nocheck
local yaml = require("https://atmosp.here/2.0/yaml.lus")

local config = yaml.decode("server:\n  port: 8080\n  hosts: [a, b]\n")
print(config.server.port)                    --> 8080
print(yaml.encode({ name = "lus", tags = { "a", "b" } }))
```

The package requires Lus 2.0. It declares no permissions. It calls no `pledge` of its own, so the program that loads it keeps control of its permissions.

The reference is in the doc comments of `yaml.lus`. Run `lus doc yaml.lus` to print it.

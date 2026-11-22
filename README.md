# yaml

`yaml` reads and writes YAML 1.2 with the core schema.

The following example reads a server configuration, then writes the settings of a blog.

```lus nocheck
local yaml = require("https://atmosp.here/2.0/yaml.lus")

local config = yaml.decode("server:\n  port: 8080\n  hosts: [web1, web2]\n")
print(config.server.port)                    --> 8080
print(yaml.encode({ title = "Field notes", tags = { "travel", "food" } }))
```

The package requires Lus 2.0 and declares no permissions. It never calls `pledge`, so the program that loads it keeps control of its permissions.

The reference is in the doc comments of `yaml.lus`, which `lus doc yaml.lus` prints.

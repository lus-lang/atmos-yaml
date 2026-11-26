# Changelog

## 1.0.0

**Release date:** TBD

Version 1.0.0 is the first release of `yaml`, which reads and writes YAML 1.2 with the core schema.

- Added `yaml.decode`, `yaml.decode_all`, `yaml.encode`, and `yaml.iserror`.
  - `yaml.decode`: Parses the first document of a text.
  - `yaml.decode_all`: Parses every document of a text into a list.
  - `yaml.encode`: Writes a value as a YAML document in block style.
  - `yaml.iserror`: Tests whether a value is an error object that `yaml.decode` or `yaml.decode_all` raised.

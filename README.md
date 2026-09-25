# MNX Checklist

This repository tracks concepts that the [MNX notation format](https://github.com/w3c/mnx) identifies as planned for version 1.0. The checklist is grouped using the [Music Notation Reference](https://w3c-cg.github.io/music-notationref/) taxonomy.

See [CHECKLIST.md](CHECKLIST.md) for the current list. Checked items are based on schema paths recorded in `implemented.json` and verified against the MNX JSON schema when the checklist is generated.

## Regenerate the checklist

Requirements: Python 3. The generator fetches the current concepts taxonomy, MNX support information, and MNX JSON schema from their upstream repositories, so network access is required.

```sh
python3 generate_checklist.py
```

To use local source files instead, pass paths with `--concepts`, `--mnx`, and `--schema`. Run `python3 generate_checklist.py --help` for all options.

## Tracking implementation

Add an entry to `implemented.json` using a notationref concept ID as the key and one or more slash-separated paths in the MNX schema as its value. The generator checks those paths and marks the corresponding checklist item when they exist. An enum value can be checked with a final `enum/VALUE` path segment. Existing checked boxes in `CHECKLIST.md` are also preserved across regeneration.

## Sources

- [MNX specification repository](https://github.com/w3c/mnx)
- [Music Notation Reference taxonomy](https://github.com/w3c-cg/music-notationref)

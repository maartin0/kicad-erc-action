# KiCad ERC Checker
Runs the KiCad ERC (electrical rules checker) on the provided `.kicad_sch` file

See [this list](https://github.com/stars/maartin0/lists/kicad-action-utils) for related actions

### Example
`.github/workflows/erc.yml`
```yml
name: Run ERC on schematic

on: push

jobs:
  run:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout to latest commit
        uses: actions/checkout@v4

      - name: Run ERC
        uses: maartin0/kicad-erc-action@v1
        with:
          sch: project_name.kicad_sch
```
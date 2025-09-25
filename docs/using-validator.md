# Using the validator (from labki-packs-tools)

CI (GitHub Actions):

```yaml
name: Validate content packs
on:
  pull_request:
  push:
    branches: [ main ]

jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/checkout@v4
        with:
          repository: Aharoni-Lab/labki-packs-tools
          path: tools-cache
      - uses: actions/setup-python@v5
        with:
          python-version: '3.11'
      - name: Install deps
        run: pip install pyyaml jsonschema
      - name: Validate manifest
        run: |
          python tools-cache/tools/validate_repo.py validate manifest.yml
```

Local:

```bash
pip install pyyaml jsonschema
python tools/validate_repo.py validate manifest.yml
```

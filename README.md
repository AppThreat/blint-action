# blint-action
Action to run BLint, the binary linter.

## Inputs

## `src`

Path(s) to images or image containing directories. Defaults to workspace.

## Example usage
```yaml
uses: appthreat/blint-action@latest
with:
  src: |
    MySourceDir
    MySourceImage


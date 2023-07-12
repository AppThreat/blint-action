
# BLint-action

![blint logo](https://raw.githubusercontent.com/AppThreat/blint/feature/blint-action/blint.ico)

BLint is a Binary Linter to check the security properties, and capabilities in your executables. It is powered by [lief](https://github.com/lief-project/LIEF).

Supported binary formats:

- ELF (GNU, musl)
- PE (exe, dll)
- Mach-O (x64, arm64)

## Inputs

## `reports_dir`

Path to output reports. Defaults to workspace/reports.

## `src`

Path(s) to images or image containing directories. Defaults to workspace.

## Example usage
```yaml
uses: appthreat/blint-action@latest
with:
  reports_dir: workspace/DesiredPath
  src: |
    MySourceDir
    MySourceImage
```

## Reports

Blint-action produces the following json artifacts in the /workspace/reports directory:

- blint-output.html - HTML output from the console logs
- exename-metadata.json - Raw metadata about the parsed binary. Includes symbols, functions, and signature information
- findings.json - Contains information from the security properties audit. Useful for CI/CD based integration
- reviews.json - Contains information from the capability reviews. Useful for further analysis
- fuzzables.json - Contains a suggested list of methods for fuzzing

## References

- [lief examples](https://github.com/lief-project/LIEF/tree/master/examples/python)
- [checksec](https://github.com/Wenzel/checksec.py)

## Discord support

The developers can be reached via the [discord](https://discord.gg/DCNxzaeUpd) channel.


# Test report — v3.1.0

17 October 2026. Windows compatibility update targeting Illustrator 2019–2026.

## Automated checks passed

- 13 geometry and input-validation test groups.
- 9 simulated CEP bridge/UI test groups: settings encoding, preview cleanup, serialized changes, creation tokens, document switching, presets, units, malformed replies and panel-hide cleanup.
- Social-link checks for all six destinations, supported CEP response formats, error handling and click-only launching. No messages were sent.
- 36 compatibility checks: version boundaries (including 2025's 29.5.1 change), unsupported-version rejection, multiple-runtime selection, manifest range, PowerShell parsing, old receipt migration, repeat-install preservation of original settings and invalid-receipt rejection. Registry writes were simulated.
- Read-only installation detection found Illustrator 30.6.0 and selected CEP 12.

## Testing limits

Only Illustrator 2026 / 30.6.0 is installed on the development computer. The unchanged drawing host passed 15 native Illustrator checks in the earlier package; that historical result is not a fresh native test of v3.1.0.

Illustrator 2019–2025 are compatibility targets. Their actual menu registration, embedded-browser rendering, docking and complete workflows have not been tested in those host applications. A wider manifest and matching registry settings do not guarantee every installation will work.

No claim of exhaustive testing is made. Fresh-machine installation and settings restoration against a real registry have not been tested for v3.1.0. Original settings are backed up before changes; receipt logic was tested with a simulated registry. Preview cleanup during abrupt application shutdown cannot be guaranteed.

## References

[Adobe CEP compatibility and extension documentation](https://github.com/Adobe-CEP/CEP-Resources/blob/master/CEP_12.x/Documentation/CEP%2012%20HTML%20Extension%20Cookbook.md)

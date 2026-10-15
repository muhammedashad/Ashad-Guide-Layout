# Extension test report

Prepared 13 October 2026. Extension version 3.0.0; Illustrator host 30.6.0.

## Passed

- The shared layout engine's 13 geometry/validation test groups.
- Nine extension test groups covering settings transport, startup cleanup, document context, checkbox preview/clear, serialized rapid updates, creation tokens, document switching, presets and unit conversion, malformed bridge replies, and panel-hide cleanup. These use a simulated browser/CEP bridge.
- Fifteen native checks inside Illustrator across two isolated test documents: document identities, preview creation and replacement, invalid-preview rollback, cross-document cleanup, stale-identity rejection, final creation, persistent ownership tags, recovery after host reload, final group tags, source artwork preservation, and preservation of existing user documents. All native host checks passed; raw results are included.
- JavaScript syntax and manifest/installer syntax checks. Package resources are local; no Node integration, remote script loading, network service, analytics, or account sign-in is required.

## Limits

The docked HTML panel has not yet been verified end-to-end in the installed CEP runtime. Its host commands were run in real Illustrator; its UI and bridge callbacks were checked in simulation. The Windows installer, first-launch menu registration, panel docking and theme events need verification after installation and Illustrator restart. Older Illustrator versions and macOS are not targeted by this installer. Preview cleanup during an abrupt application shutdown cannot be guaranteed; reopen cleanup is included. No claim of exhaustive bug coverage is made.

## Reference

Adobe CEP 12 documents the Panel type as dockable and describes loading unsigned local extensions:
https://github.com/Adobe-CEP/CEP-Resources/blob/master/CEP_12.x/Documentation/CEP%2012%20HTML%20Extension%20Cookbook.md


## Social buttons update — 15 October 2026

Version 3.0.1: all seven destinations exactly match the supplied links. Automated checks passed for click-only launching, numeric and object CEP result codes, error messages, unavailable CEP bridge, and unsupported URL handling. The nine existing extension test groups also passed. Installer PowerShell syntax passed. No profiles were contacted or messages sent during these simulated checks. Browser/email launching from the installed Illustrator panel remains unverified.


## Compact social icons — 15 October 2026

Version 3.0.2 removes only the Email button and replaces the six remaining text buttons with 32 px circles containing 18 px inline vector icons. Labels are available to assistive technology and as hover tooltips. The existing six-destination launch checks and nine extension test groups passed. Actual rendering of this update in Illustrator has not been verified.

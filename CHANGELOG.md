# Changelog

## 0.2.0

- Correct the minimum supported runtime to Mog 0.1.4, the first release that
  embeds its configured package-compatibility version correctly.
- Add pinned CI/release automation with tag checks, 0.1.4/current-runtime tests,
  checksummed archives, and automated action updates.
- Add explicit failure, inequality, boolean, null, and approximate assertions.
- Include actual and expected values in equality diagnostics.
- Reject negative or NaN approximate-equality tolerances and NaN operands.
- Correct the manifest license identifier to match the GPL-3.0 license text.
- Document installation, supported helpers, and the assertion-only scope.
- Expand package tests across every non-failing assertion path.

## 0.1.1

- Require Mog runtime 0.1.1 or newer for `any` parameters in assertion helpers.
- Add complete package publication metadata.

## 0.1.0

- Initial foundation package contract.

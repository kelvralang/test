# moglang/test

Small, dependency-free assertion helpers for Mog tests. The canonical import is
`github.com/moglang/test`, and the package supports Mog runtime `^0.1.4`.

```bash
mog add github.com/moglang/test@v0.2.0 --dev
```

```mog
const test = @import("github.com/moglang/test")

test.equal(2 + 2, 4, "addition")
test.notEqual("ready", "waiting", "states differ")
test.isTrue(10 > 3, "comparison")
test.isNull(null, "optional is empty")
test.approxEqual(0.1 + 0.2, 0.3, 0.000001, "floating point sum")
```

Available helpers are `fail`, `assert`, `equal`, `notEqual`, `isTrue`,
`isFalse`, `isNull`, `notNull`, and `approxEqual`. Equality helpers include
the actual and expected values in their failure diagnostics. `approxEqual`
uses an absolute tolerance and rejects negative or NaN tolerances and NaN
operands.

This package intentionally provides assertions rather than test discovery or
a runner. Project-level test entry points remain configured through Mog's
`[scripts].test` manifest entry. The complete public contract is declared in
`package.api.mog`. The package is licensed under GPL-3.0-only; see `LICENSE`.

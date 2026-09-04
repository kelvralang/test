# kelvralang/test

Small, dependency-free assertion helpers for Kelvra tests. The canonical import is
`github.com/kelvralang/test`, and the package supports Kelvra runtime `^0.2.0`.

```bash
kelvra add github.com/kelvralang/test@v0.2.0 --dev
```

```kelvra
const test = @import("github.com/kelvralang/test")

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
a runner. Project-level test entry points remain configured through Kelvra's
`[scripts].test` manifest entry. The complete public contract is declared in
`package.api.kel`. The package is licensed under GPL-3.0-only; see `LICENSE`.

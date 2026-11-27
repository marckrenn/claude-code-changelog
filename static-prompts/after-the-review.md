

## After the review

After the findings are reported (and applied, when --fix was passed): if `/${…}` has not run this session and the diff has a runtime surface (not test-only or docs-only per the pre-ship exemptions), invoke `/${…}` now — this review checks that the diff reads right; `/${…}` checks that it runs right.

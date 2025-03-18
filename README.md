# pinact run --verify

## Install

```bash
$ brew install suzuki-shunsuke/pinact/pinact
$ pinact --version
pinact version 1.4.0 (ed62a78045ee6c200f8e561ac292ef9017ac19af)
```

## Reproduce Steps

```bash
GITHUB_TOKEN=$(gh auth token) pinact run --verify .github/workflows/test.yaml
```

## Expected

Show Error!

- https://github.com/suzuki-shunsuke/pinact/blob/main/docs/codes/001.md

## Actual

Rewrite the workflow file.

```diff
--- i/.github/workflows/test.yaml
+++ w/.github/workflows/test.yaml
@@ -6,6 +6,6 @@ jobs:
     runs-on: ubuntu-latest
     steps:
       - name: checkout
-        uses: actions/checkout@v4
+        uses: actions/checkout@11bd71901bbe5b1630ceea73d27597364c9af683 # v4.2.2
       - name: test
         run: echo "test!"
```

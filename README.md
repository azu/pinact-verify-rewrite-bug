# pinact run --verify

## Install

```bash
$ brew install suzuki-shunsuke/pinact/pinact
$ pinact --version
pinact version 1.4.0 (ed62a78045ee6c200f8e561ac292ef9017ac19af)
``

## Reproduce Steps

```bash
GITHUB_TOKEN=$(gh auth token) pinact run --verify .github/workflows/test.yaml
```

## Expected

Show Error!

## Actual


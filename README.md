# Homebrew tap for cadenas

[cadenas](https://github.com/PierreEbele/cadenas) encrypts a file with a
password: Argon2id and XChaCha20-Poly1305, any file size, and compatible
with [age](https://age-encryption.org).

## Install

```bash
brew install pierreebele/cadenas/cadenas
```

Works on macOS (Apple Silicon and Intel) and Linux. The formula installs the
[npm package](https://www.npmjs.com/package/cadenas), published with
provenance, using Homebrew's Node.js.

```bash
cadenas lock report.pdf               # → report.pdf.cadenas
cadenas unlock report.pdf.cadenas     # → report.pdf
cadenas --help
```

## Updating the formula (maintainers)

`Formula/cadenas.rb` is updated automatically at each release of cadenas:
the `homebrew` job of the main repository's
[release workflow](https://github.com/PierreEbele/cadenas/blob/main/.github/workflows/release.yml)
generates it, installs it, runs `brew test` and `brew audit --strict --online`
on macOS, then pushes it here. The [Tests](.github/workflows/tests.yml)
workflow checks it again on macOS and Linux.

Issues and security reports: see the
[main repository](https://github.com/PierreEbele/cadenas).
# Guvna releases

Signed release binaries for **guvna**, the local-first CLI for Guvna's cloud
governance tools. Visit [guvnacloud.com](https://guvnacloud.com).

This repository contains **release binaries only**. The source code is not
published here.

## Install

```sh
# Homebrew (macOS and Linux)
brew install guvnacloud/tap/guvna        # stable releases
brew install guvnacloud/tap/guvna-beta   # beta releases

# Install script (macOS and Linux): verifies checksums, never uses sudo
curl -fsSL https://github.com/GuvnaCloud/releases/releases/latest/download/install.sh | sh
```

Or download an archive for your platform from [Releases](https://github.com/GuvnaCloud/releases/releases).
Archives are available for macOS and Linux (amd64 and arm64) and Windows (amd64).

## Verify

Every release includes:

- `checksums.txt`: SHA-256 checksums of every asset
- `checksums.txt.sigstore.json`: a keyless [Sigstore](https://www.sigstore.dev/) signature over `checksums.txt`
- `checksums.txt.intoto.sigstore.json`: signed SLSA v1 build provenance
- `*.sbom.json`: a software bill of materials for each archive
- `THIRD_PARTY_NOTICES`: licences of bundled third-party components

See [guvnacloud.com/docs/verify](https://guvnacloud.com/docs/verify) for the
exact verification commands.

## Report a security issue

Email security@guvnacloud.com. Please do not open a public issue.

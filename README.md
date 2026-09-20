# BrewVisual Releases

Private staging repository for BrewVisual release artifacts, release notes, and public product information.

## Artifact contract

- Release archives use the name `BrewVisual-<version>.zip`.
- Every published archive must contain the signed and notarized `BrewVisual.app` bundle.
- The source code remains in the permanently private `felix-lorenz/brewvisual` repository.
- No distribution artifact is uploaded until Developer ID signing and notarization have completed successfully.

## Publication gate

Before this repository becomes public, verify that the release page and archive are accessible without GitHub authentication, recalculate the public archive SHA-256, and update the matching cask in `felix-lorenz/homebrew-tap`.

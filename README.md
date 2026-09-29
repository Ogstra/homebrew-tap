# Ogstra Homebrew tap

Homebrew cask for [Proxor](https://github.com/Ogstra/proxor), a proxy client with a Qt GUI built on the sing-box core.

## Install

```bash
brew install --cask ogstra/tap/proxor
```

Requirements: Apple Silicon Mac, macOS 15 (Sequoia) or later, Homebrew 7 or newer (run `brew update` first).

## Update

```bash
brew upgrade --cask proxor
```

## Uninstall

```bash
brew uninstall --cask proxor
```

To also remove `~/Library/Preferences/proxor` and `~/Library/Preferences/io.github.Ogstra.Proxor.plist`:

```bash
brew uninstall --cask --zap proxor
```

## Notes

- Proxor is ad-hoc signed and not notarized (no paid Apple Developer account). The cask removes the `com.apple.quarantine` attribute after installing so macOS opens it. A zip downloaded manually from the Releases page is blocked by Gatekeeper until you run `xattr -dr com.apple.quarantine Proxor.app` or right-click > Open.
- The cask follows every published Proxor release, prereleases included.
- If you tapped with `brew tap ogstra/tap` and use short names, Homebrew asks you to trust it once: `brew trust --cask ogstra/tap/proxor`.
- The cask is updated automatically by the Proxor release pipeline. Changes to it are made in `packaging/homebrew/proxor.rb.in` of the Proxor repository, not here.

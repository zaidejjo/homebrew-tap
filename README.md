# homebrew-tap

Personal Homebrew tap for my apps. One repo serves every package —
each app gets its own Cask under `Casks/`, published automatically
by that app's release pipeline (GoReleaser).

## Usage

```sh
brew tap zaidejjo/tap
brew install --cask <package>
```

## Packages

| Package | Install | Source |
|---|---|---|
| zgit | `brew install --cask zaidejjo/tap/zgit` | [zaidejjo/zgit](https://github.com/zaidejjo/zgit) |

## Adding a new package

1. In the app's repo, add a `homebrew_casks` block to `.goreleaser.yaml`
   pointing at `zaidejjo/homebrew-tap` (see zgit's config for reference).
2. On the next tag release GoReleaser drops `Casks/<app>.rb` here.
3. Add a row to the table above.

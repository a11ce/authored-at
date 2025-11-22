# Authored-at

This repository proposes the `Authored-at` [Git trailer](https://git-scm.com/docs/git-interpret-trailers) to describe the physical location at which the contents of a commit were written. Possible values include `Home`, `<CompanyName> HQ`, or `Noisebridge`.

`prepare-commit-msg` is a [Git hook](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks) that adds the `Authored-at` trailer based on a user-specified map of network names to their locations.

1. Edit `SSID_LOCATION_MAP` to add your locations.
2. To add the hook to a single repo, copy it to `.git/hooks/prepare-commit-msg` in that repo.
3. To use it globally, set `git config --global core.hooksPath path/to/this/folder`

The included hook only works on macOS. To port it, edit getSSID. Please send a PR if you do this.

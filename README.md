> Some notes on Github CLI!

## Checking Status of Actions for Feature Branch

Obtain the top 3 status of feature branch action:
```bash
gh run list -R BruceChanJianLe/HyprMac -b feature/move-window-top-bottom-monitor -L 3
```

## Downloading Artifacts

From the ID for which action artifacts to download:
```bash
gh run download -R BruceChanJianLe/HyprMac 35964401769 -n HyprMac-app
```

## Creating a New Release

Example:
```bash
gh release create v0.14.2-1 \
    --repo BruceChanJianLe/HyprMac \
    --target feature/move-window-top-bottom-monitor \
    --title "HyprMac 0.14.2-1" \
    --notes "Window rules for already-open windows, move window to monitor above or below." \
    path/to/HyprMac-0.14.2-1.zip
```

Options:
```bash
gh release create v0.14.1-2 --draft ...              # visible only to you until you publish it
gh release create v0.14.1-2 --prerelease ...         # marked as pre-release, not shown as "Latest"
gh release upload v0.14.1-2 file.zip --clobber       # add or replace an asset on an existing release
gh release edit v0.14.1-2 --notes "..."              # change title or notes later
gh release view v0.14.1-2 --web                      # open the page in the browser
gh release delete v0.14.1-2 --cleanup-tag --yes      # remove release and its tag
```

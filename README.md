# xivplugins

Custom Dalamud plugin master repo. Contains only metadata + icons; plugin
binaries are served from GitHub Releases in each plugin's repo.

## Adding this repo to Dalamud

In-game, `/xlsettings → Experimental → custom repo URLs`, add:

```
https://raw.githubusercontent.com/porys/xivplugins/main/pluginmaster.json
```

## Adding / updating a plugin

1. Plugins publish themselves via their own release workflow (tag `v*` →
   build → `gh release create` → upload zip).
2. Add one entry to `pluginmaster.json`, pointing `DownloadLinkInstall`/
   `DownloadLinkUpdate` at that repo's
   `releases/latest/download/<name>.zip` (static URL, no per-version churn).
3. Drop `icon.png` here if you want icons, reference it via `IconUrl`.

## Layout

- `pluginmaster.json` — one object per plugin entry.
- `icon.png` — icon for each plugin (one per plugin, as needed).
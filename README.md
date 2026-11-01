# JordanNewell's Scoop bucket

Personal [Scoop](https://scoop.sh) bucket for JordanNewell's Windows tools.

## Usage

```powershell
scoop bucket add jordannewell https://github.com/JordanNewell/bucket
scoop install curt-openwith
```

## Packages

| Package | Description |
|---------|-------------|
| [curt-openwith](https://github.com/JordanNewell/curt-openwith) | Double-click a `.curt` file and it opens in the offline Curt Viewer — a browser page that renders the conversation locally. |

### curt-openwith post-install

Scoop only unpacks the package — it does **not** register the `.curt` file
association. To register it (current user only, no admin), run:

```powershell
& "$(scoop prefix curt-openwith)\install.cmd"
```

`CurtViewer.exe` is the portable native launcher; it resolves its siblings
(`curtopen.ps1`, `viewer/`) relative to its own directory, and the scoop shim
invokes the exe in place, so shimming is safe.

## Versioning

Manifest hashes are pinned to GitHub release artifacts. Updates are manual
(hashes verified by hand against the release zip) — there is no autoupdate
block yet. See each manifest for the pinned version.

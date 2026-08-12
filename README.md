# Scoop bucket for Leteo

[Leteo](https://github.com/asanabrial/leteo) is local-first persistent memory
for AI coding agents: one Rust binary over one SQLite database.

```powershell
scoop bucket add leteo https://github.com/asanabrial/scoop-leteo
scoop install leteo
```

## What this repository is

One manifest, and Scoop's own Excavator keeping it current. `checkver` watches
the releases and `autoupdate` rewrites the URL and takes the checksum from the
`SHA256SUMS` the release publishes — the same file `install.ps1` verifies
against, so a package installed this way and one installed by the script are
the same bytes checked the same way.

Everything else — what Leteo is, how it works, what it promises — lives in
[the main repository](https://github.com/asanabrial/leteo). A bucket that
duplicates a README is a bucket with a second copy to keep true.

## What Scoop does and does not take away

`scoop uninstall leteo` removes the binary and nothing else. The store lives in
`~/.leteo` and stays, which is deliberate: uninstalling a package should not
throw away somebody's memories. `leteo uninstall` is the command that offers to.

# polyclav Scoop bucket

Scoop manifests for [polyclav](https://github.com/mschulkind-oss/polyclav), a
live piano host for Windows, macOS, and Linux.

## Install

```powershell
scoop bucket add polyclav https://github.com/mschulkind-oss/scoop-bucket
scoop install polyclav
```

Then, once:

```powershell
polyclav bootstrap   # starter soundfonts, ~500 MB
polyclav            # start the daemon; web UI at http://127.0.0.1:8666/
```

Nothing makes sound until you name your keyboard in `[midi].allow_devices` —
the web UI has a picker that writes it for you.

## What is in here

`bucket/polyclav.json` is generated from the published Windows release zip by
`scripts/scoop-manifest.sh` in the polyclav repo, because it has to carry the
sha256 of the asset that was actually released. Do not hand-edit it; regenerate
it.

See [`docs/SCOOP.md`](https://github.com/mschulkind-oss/polyclav/blob/main/docs/SCOOP.md)
for the details and the update procedure.

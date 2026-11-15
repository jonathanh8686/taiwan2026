# taiwan2026

Trip site for Taiwan 2026, served at https://taiwan.jonathanhsieh.dev.

## Deployment

Hosted on the `omashu` GCE VM (Apache), same setup as `vietnam2026`:

- **Deploy = push to `main`.** `taiwan2026-deploy.timer` fast-forwards the server clone at `/home/jonathanh1386/taiwan2026` every minute.
- Apache DocumentRoot `/var/www/taiwan2026` is a symlink to that clone.
- `/.git` paths return 404 (global `block-git.conf`).

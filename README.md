# BTN Website

Static HTML website for Biological Transport Networks at the Flatiron Institute.

- Source: https://github.com/ajmayer95/BTN-Website
- Flatiron site: https://users.flatironinstitute.org/~btn/
- Local working copy: `~/Projects/BTN-Website` (outside Google Drive).

## Preview locally

From the repository directory:

```bash
python3 -m http.server 8765 --bind 127.0.0.1
```

Open http://127.0.0.1:8765/ (or `/yolk-sac.html`). Keep the terminal running; Control-C stops it. Use Command-Shift-R to refresh cached media.

## Review and merge

Work on a branch, commit intended HTML and web-ready media, push, and open a pull request into `main`. Review and merge before publishing. Avoid committing temporary files, private notes, credentials, or large source videos.

## Deploy to Flatiron

**Merging on GitHub does not update the Flatiron site.** The Flatiron web service serves `/mnt/home/btn/public_www` on the cluster. The `amayer` account has write access; no interactive login as `btn` is needed. This is `public_www`, not `public_html`.

From a Mac on FI's internal network or FI VPN:

```bash
ssh amayer@rusty
```

Outside FI without VPN, connect through the gateway, authenticate interactively, then connect to Rusty:

```bash
ssh -p 61022 amayer@gateway.flatironinstitute.org
ssh rusty
```

Run the following **on Rusty**, in the same shell, stopping if any command fails.

1. Back up the published site outside its public directory:

```bash
cp -a /mnt/home/btn/public_www \
  "$HOME/btn-site-backup-$(date +%Y%m%d-%H%M%S)"
```

2. Obtain the latest merged source in a new staging directory:

```bash
btn_source=$(mktemp -d "$HOME/btn-publish-XXXXXX")
git clone --branch main --single-branch \
  https://github.com/ajmayer95/BTN-Website.git "$btn_source"
```

3. Inspect the transfer:

```bash
rsync -av --dry-run \
  --exclude='.git/' --exclude='.DS_Store' \
  "$btn_source/" /mnt/home/btn/public_www/
```

4. Publish and ensure public read access:

```bash
rsync -av \
  --exclude='.git/' --exclude='.DS_Store' \
  "$btn_source/" /mnt/home/btn/public_www/
chmod -R a+rX /mnt/home/btn/public_www
```

Files are automatically served; no web-server restart is needed. Verify the public pages and media, then `exit`. If connected through the gateway, `exit` again to return to your Mac.

The transfer preserves existing destination files. Deleted source files therefore remain publicly available until explicitly removed; do not add `--delete` without reviewing the full destination and backup. Only commit files intended for public distribution: the deployment copies repository contents other than the exclusions above.

GitHub Pages is a separate mirror at https://ajmayer95.github.io/BTN-Website/ and is configured to publish from `main`. It does not synchronize the Flatiron directory or the Simons Foundation website. Simons edits are handled by its web team.

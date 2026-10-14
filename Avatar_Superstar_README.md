# Whitelist

Live user whitelist for the Unity project. Fetched at runtime straight from
the raw GitHub URL — no rebuild needed to change who's allowed.

## How to update
1. Edit `whitelist.txt` (one entry per line).
2. Commit to the default branch.
3. The running app picks it up on its next fetch.

## Raw URL (what Unity fetches)
https://raw.githubusercontent.com/<user>/<repo>/<branch>/whitelist.txt

## Format
- One username / ID / key per line
- Blank lines ignored
- Lines starting with `#` are comments, ignored

## Heads-up: CDN cache
`raw.githubusercontent.com` caches for ~5 minutes, so edits aren't instant.
If you need an immediate refresh, append a cache-buster to the URL, e.g.
`...whitelist.txt?t=TIMESTAMP`.

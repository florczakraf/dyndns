# dyndns
This repo contains a small script that I run in cron on my home server to update the
dynamic home address via Cloudflare API.

# Usage
Create `.env` from the provided `.env.example` and fill required fields.
Add to cron like:
```
* * * * * /path/to/update-dyndns >/dev/null 2>/dev/null
```
or if you want to use journal logging:
```
* * * * * systemd-cat -t "dyndns" /path/to/update-dyndns >/dev/null 2>/dev/null
```

# Requirements
- bash
- curl

# License
MIT, see [`LICENSE`](./LICENSE)

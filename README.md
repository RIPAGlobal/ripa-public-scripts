# ripa-public-scripts
A helper script repo for various public scripts we need before we've authed with github.

This is to stop us needing to have the same code in multiple repos, it's mainly
for our in-house tools but if you find it useful then great! If you find any
bugs or want to suggest improvements please submit a PR or feel free to fork the
repo and modify for your use cases.

See individual scripts in the bin/ folder for documentation relating to each
script (mostly contained within the scripts).

### Useage
Generally as we need to use these to auth with github we'll be pulling them from
the public raw file site and piping them straight into bash or storing them for
local use.
  Example:
```bash
 curl https://raw.githubusercontent.com/RIPAGlobal/ripa-public-scripts/<tag, commit or branch>/bin/<script> \
   | bash [-s -- --<options> ...]
```

***WARNING*** If you target a branch be prepared for unnanounced breaking changes.

### Available Scripts

See the individual scripts for more info or curl and pipe to bash with `-s -- --help`

| Script Name | Use Case |
| --- | --- |
| gh-auth-and-status-update | A script to auth as a github app and write to commit statuses |

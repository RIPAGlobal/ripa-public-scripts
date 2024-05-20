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

You might want to check the sha256sum with what you get from curl just to be
safe something like:
``` bash
echo <curl result> | sha256sum --check <( \
  echo "<sha256>  -" \
)
```
Get the SHA256 from the table below or to be super safe check out the repo,
inspect the contents and then generate your own SHA256 and use that in your
calling scripts to verify as per above.

***WARNING*** If you target a branch be prepared for unnanounced breaking changes.

### Available Scripts

See the individual scripts for more info or curl and pipe to bash with `-s -- --help`

| Script Name | Use Case | sha256sum hash |
| --- | --- | --- |
| gh-auth-and-status-update | A script to auth as a github app and write to commit statuses | c131992336f2b8b11d020617bd34456e021dd965e7a6d25db9c9eb2a80cb686f |

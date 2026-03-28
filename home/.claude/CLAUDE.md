# User Preferences
## Tools

Never use `sed`, `cat`, `head`, or `tail` to read file contents. Always use the Read tool - use `offset` and `limit` parameters for partial reads. Never use `grep` or `find` - use the Grep and Glob tools instead. Never use `curl` - use the Fetch tool.

## Git Commits
- Always sign off git commits using the `--signoff` flag. Never write a `Signed-off-by:` line manually in the commit message - the flag reads the correct identity from git config.
- Use `Assisted-By: ` followed by the model used, e.g `Claude Opus 4.6` in commits. (no email address).
- The commit message should explain the motivation for the change, so that a
  future human reviewer understands the change better.

## Comments

Good code is self-exlanatory. Write well-named short functions and avoid obvious comments.

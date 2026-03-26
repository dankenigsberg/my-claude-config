# My non-authoritative config for Claude

I'd like Claude to work fine for me on multiple desktops.
This is not intended to be general or useful for everyone. However, suggestions
are always welcome.

## License
You can copy this repo only if you use it for creation of open-source software.

## Usage
Apply the included config to each desktop with
```
stow -d ./home -t "$HOME" .
```

## Plugins
I wish I knew how to pull them via config files. Until then,
```
claude plugin marketplace add EveryInc/compound-engineering-plugin
claude plugin install compound-engineering
```

## Jira
Run
```
claude mcp add atlassian --transport http https://mcp.atlassian.com/v1/mcp --scope user
```
and in the claude shell, use `/mcp` to choose `atlassian` and follow order to connect it to `redhat.atlssian.net`.

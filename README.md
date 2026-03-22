# My non-authoritative config for Claude

I'd like Claude to work fine for me on multiple desktops.

Apply to each desktop with

```
stow -d ./home -t "$HOME" .
```


## Jira
Generate token at https://id.atlassian.com/manage-profile/security/api-tokens
```
TOKEN=my-token
USERNAME=me@redhat.com
claude mcp add atlassian --scope user \
    -e JIRA_URL=https://redhat.atlassian.net/ \
    -e JIRA_USERNAME=$USERNAME \
    -e JIRA_API_TOKEN=$TOKEN \
    -e CONFLUENCE_URL=https://redhat.atlassian.net/wiki \
    -e CONFLUENCE_USERNAME=$USERNAME \
    -e CONFLUENCE_API_TOKEN=$TOKEN \
    -- /usr/bin/podman run -i --rm \
    -e JIRA_URL -e JIRA_USERNAME -e JIRA_API_TOKEN \
    -e CONFLUENCE_URL -e CONFLUENCE_USERNAME -e CONFLUENCE_API_TOKEN \
    ghcr.io/sooperset/mcp-atlassian:latest
```

# community-subdomain-template

Template repository for WikiPathways subdomains

## Developers
Subdomain redirect strategy for communities (portals), etc.

1. Create new repo from the [community-subdomain-template](https://github.com/wikipathways/community-subdomain-template) 
1. Add `CNAME` file with desired subdomain name. Create [manually](./CNAME) or use Settings/Pages
1. Edit the [index.html](index.html) file with redirect details
1. In CloudFlare, add CNAME record to cloudflare with name = subdomain (e.g., `cptac`), target = `wikipathways.github.io` and proxy = `DNS only`
1. Back at the repo, go to Settings/Pages, choose the `main` branch, enter the custom domain, and enforce HTTPS

The DNS will direct sudomain traffic to the target GitHub org and then GitHub will manage the final direction to the repo containing the matching CNAME file. The repo can contain web content or a simple index.html file with redirect info (like this example).

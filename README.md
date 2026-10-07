# Trulobot waiting page

This folder is the source for the public, static waiting page. It has no wallet connection, signup form, buy link, token contract address, or server endpoints. The site uses the same mascot as the X profile.

Preview locally from the repository root:

```bash
python3 -m http.server 4173 --directory apps/waiting
```

Open `http://localhost:4173` and check desktop and mobile widths. The public copy must continue to distinguish proposed token rules from a launched token. Before a token launches, every Trulobot contract address shown here should remain absent. After deployment, publish the exact checksum address on this page and [@Trulobot](https://x.com/Trulobot) in the same release step, with a BaseScan link and verified fee configuration.

Publishing target: the public [`tiago-o-pinheiro/trulobot-waiting`](https://github.com/tiago-o-pinheiro/trulobot-waiting) GitHub repository, served through GitHub Pages. The canonical domain is [trulobot.com](https://trulobot.com); its certificate is approved, HTTPS is enforced, and the X profile links to it. Copy `index.html`, `styles.css`, `assets/`, and `CNAME` when publishing updates. The canonical and Open Graph URLs already name the owned domain.

The DNS zone has GitHub Pages' four apex (`@`) A records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, and `185.199.111.153`. The `www` CNAME points directly to `tiago-o-pinheiro.github.io` (no repository path). A GitHub Pages challenge TXT record verifies domain ownership for the account; keep it in DNS. Existing NS, `_domainconnect`, SOA, and `_dmarc` records were preserved. Both hostnames resolve, `www` redirects to the apex, and HTTP redirects to HTTPS. See [GitHub's current domain instructions](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site); recheck their IP values if the DNS zone changes later.

Anyone can deploy a token with the same name or ticker. The domain, X account, and eventual exact Base contract address are the project's verification path; ownership of a domain does not reserve a token name on chain.

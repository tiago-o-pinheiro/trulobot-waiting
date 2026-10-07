# Trulobot waiting page

This folder is the source for the public, static waiting page. It has no wallet connection, signup form, buy link, token contract address, or server endpoints. The site uses the same mascot as the X profile.

Preview locally from the repository root:

```bash
python3 -m http.server 4173 --directory apps/waiting
```

Open `http://localhost:4173` and check desktop and mobile widths. The public copy must continue to distinguish proposed token rules from a launched token. Before a token launches, every Trulobot contract address shown here should remain absent. After deployment, publish the exact checksum address on this page and [@Trulobot](https://x.com/Trulobot) in the same release step, with a BaseScan link and verified fee configuration.

Publishing target: the public `tiago-o-pinheiro/trulobot-waiting` GitHub repository, served through GitHub Pages. The project URL can be used as a staging preview. The canonical domain is `trulobot.com`; point DNS to GitHub Pages and enable HTTPS before adding the URL to the X profile or announcing the waiting page. Copy only `index.html`, `styles.css`, and `assets/` when publishing updates. The canonical and Open Graph URLs already name the owned domain, so a staging link should not be announced as the official source.

To connect the domain, first set `trulobot.com` as the custom domain in the repository's Pages settings. At the DNS provider, replace the default apex (`@`) A records with GitHub Pages' four A records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, and `185.199.111.153`. Point the `www` CNAME directly to `tiago-o-pinheiro.github.io` (no repository path). Preserve MX, TXT, and unrelated subdomain records. Confirm both hostnames resolve and HTTPS works, then enable Enforce HTTPS in Pages if it is not already enabled. See [GitHub's current domain instructions](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site); recheck their IP values before making the change.

Anyone can deploy a token with the same name or ticker. The domain, X account, and eventual exact Base contract address are the project's verification path; ownership of a domain does not reserve a token name on chain.

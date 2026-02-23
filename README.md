# MTA-STS Policy Hosting for vigogroup.com.au
Static site for MTA-STS policy served via Cloudflare Pages.
## Deploy
1. Fork or create new repo from this.
2. Cloudflare Pages → Connect Git → Deploy (No framework).
3. Custom domain: `mta-sts.vigogroup.com.au` → CNAME to
`*.pages.dev`.
## DNS Records
Type: CNAME
Name: mta-sts
Target: your-project.pages.dev (proxied)
Type: TXT
Name: _mta-sts
Value: "v=STSv1; id=20260223T1500"
## Updating Policy
- Edit `.well-known/mta-sts.txt`
- Update `id=` timestamp in `_mta-sts` TXT
- Redeploy via Git push
## Test
curl https://mta-sts.vigogroup.com.au/.well-known/mta-sts.txt
mxtoolbox.com/mta-sts

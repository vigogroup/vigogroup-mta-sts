# MTA-STS Policy for vigogroup.com.au

This repository hosts the MTA-STS policy published for `vigogroup.com.au`.

Production policy:

`https://mta-sts.vigogroup.com.au/.well-known/mta-sts.txt`

## Updating the policy

1. Edit `.well-known/mta-sts.txt`.
2. Update the `id=` value in the `_mta-sts.vigogroup.com.au` TXT record when the policy changes.
3. Deploy the updated static site through Cloudflare Pages.
4. Verify the published policy endpoint.

This is an operational infrastructure repository for Vigo Group.

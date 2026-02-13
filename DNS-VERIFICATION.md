# DNS Verification for GitHub Pages

This document contains instructions for verifying the domain cloverlu.com with GitHub Pages.

## DNS TXT Record Configuration

Before GitHub Pages can verify your custom domain, you need to add a DNS TXT record to your domain's DNS configuration.

### Required TXT Record

Add the following TXT record to your DNS configuration:

**Hostname:**
```
_github-pages-challenge-jamescreationshow-cmyk.cloverlu.com
```

**Value:**
```
1b71ca22a0157de9b6ad852474c087
```

### Steps to Add the TXT Record

1. Log in to your domain hosting service (e.g., Namecheap, GoDaddy, Cloudflare, etc.)
2. Navigate to your DNS settings or DNS management page
3. Add a new TXT record with:
   - **Name/Host:** `_github-pages-challenge-jamescreationshow-cmyk`
   - **Type:** TXT
   - **Value/Content:** `1b71ca22a0157de9b6ad852474c087`
   - **TTL:** Default (or 3600)
4. Save the DNS record

### Verification

After adding the TXT record, DNS changes may take anywhere from a few minutes to 24 hours to propagate.

You can verify the DNS configuration has been updated by running this command:

```bash
dig _github-pages-challenge-jamescreationshow-cmyk.cloverlu.com +nostats +nocomments +nocmd TXT
```

If your DNS configuration has updated correctly, you should see the TXT record with the verification code in the output.

### Additional Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages)
- [Managing a custom domain for your GitHub Pages site](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)

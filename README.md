# shakil-mdshosen.github.io

Personal website hosted on GitHub Pages with custom domain: **http://shakil.live/**

## 🌐 Custom Domain Setup

This repository is configured to use the custom domain `shakil.live` through GitHub Pages. The `CNAME` file contains the domain configuration.

### DNS Configuration Required

To make your domain work, you need to configure DNS settings at your domain registrar (name.com):

#### Option 1: Using A Records (Recommended for root domain)
Add these A records for `shakil.live`:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

#### Option 2: Using CNAME (for www subdomain)
Add a CNAME record:
```
www.shakil.live → shakil-mdshosen.github.io
```

### GitHub Pages Settings
1. Go to your repository settings
2. Navigate to "Pages" section
3. Ensure "Source" is set to "Deploy from a branch"
4. Select "main" branch and "/ (root)" folder
5. The custom domain should show `shakil.live`
6. Enable "Enforce HTTPS" once DNS propagation is complete (24-48 hours)

## 📧 Free Email Hosting Options

Since you want free email for your domain `shakil.live`, here are the best options:

### Option 1: Cloudflare Email Routing (Recommended - 100% Free Forever)

**Features:**
- Completely free email forwarding service
- Unlimited email addresses
- Unlimited email forwarding
- No storage limits (forwards to your existing email)
- Easy setup with Cloudflare DNS
- Professional and reliable

**Setup Steps:**
1. Sign up for a free Cloudflare account at [cloudflare.com](https://cloudflare.com)
2. Add your domain `shakil.live` to Cloudflare (free plan)
3. Update your nameservers at name.com to Cloudflare's nameservers
4. In Cloudflare dashboard, go to Email Routing
5. Enable Email Routing for your domain
6. Add destination email address (where you want to receive emails)
7. Create email addresses like `you@shakil.live` and forward them to your existing email
8. Verify your destination email address

**Pros:**
- Truly free forever
- Easy to set up
- Reliable infrastructure
- Can create unlimited email addresses

**Cons:**
- Email forwarding only (can't send from custom domain without additional setup)
- Need to transfer DNS to Cloudflare

### Option 2: ImprovMX (Free Email Forwarding)

**Features:**
- Free email forwarding
- Up to 3 domain aliases on free plan
- Unlimited email forwards
- Simple setup

**Setup Steps:**
1. Sign up at [improvmx.com](https://improvmx.com)
2. Add your domain `shakil.live`
3. Add these MX records at name.com:
   ```
   Priority 10: mx1.improvmx.com
   Priority 20: mx2.improvmx.com
   ```
4. Create email aliases that forward to your existing email

**Note:** To send emails from your custom domain, you'll need to configure SMTP with your existing email provider or use the paid plan.

### Option 3: ForwardEmail.net (Free & Open Source)

**Features:**
- 100% free and open source
- Unlimited domains and aliases
- Privacy-focused
- No tracking or ads

**Setup Steps:**
1. Sign up at [forwardemail.net](https://forwardemail.net)
2. Add your domain `shakil.live`
3. Add these DNS records at name.com:
   ```
   MX Records:
   Priority 10: mx1.forwardemail.net
   Priority 20: mx2.forwardemail.net
   
   TXT Record:
   forward-email=your-email@example.com
   ```
4. Verify your domain

### Option 4: Zoho Mail (Limited Free Tier)

**⚠️ Note:** Zoho Mail's free tier has become more limited and may require payment for custom domain features. Many users report that the free custom domain email service is no longer available for new sign-ups.

**If still available:**
- Sign up at [zoho.com/mail](https://zoho.com/mail)
- Check current free tier limitations
- May require paid plan for custom domain email

### Option 5: Gmail with Custom Domain (Google Workspace - Paid)

**Note:** Google Workspace is now paid-only, starting at $6/user/month. No free tier available for custom domains.

### Option 6: ProtonMail Custom Domain (Paid)

**Note:** ProtonMail requires a paid plan (Mail Plus or higher) for custom domain email. Free tier does not support custom domains.

## 🚀 Deployment

This site automatically deploys when you push changes to the main branch. The deployment process:

1. Push code to main branch
2. GitHub Actions builds and deploys the site
3. Changes appear at `https://shakil.live` (once DNS is configured)

## 📁 File Structure

```
├── CNAME              # Custom domain configuration
├── index.html         # Main website file
├── README.md          # This documentation
└── .git/              # Git repository data
```

## 🛠️ Development

To develop locally:
1. Clone this repository
2. Make changes to `index.html` or add new files
3. Test locally by opening `index.html` in a browser
4. Commit and push changes to deploy

## ⚠️ Important Notes

1. **DNS Propagation:** DNS changes can take 24-48 hours to propagate globally
2. **HTTPS:** Enable "Enforce HTTPS" in GitHub Pages settings only after DNS is working
3. **Email Setup:** Choose one email option and configure DNS records accordingly
4. **Domain Verification:** Some email providers require domain verification via TXT records

## 🆘 Troubleshooting

### Domain not working?
- Check DNS settings at name.com
- Wait for DNS propagation (up to 48 hours)
- Verify GitHub Pages settings

### Email not working?
- Verify MX records are correctly set
- Check spam folder for verification emails
- Ensure TXT verification records are added

### SSL Certificate issues?
- Wait for DNS propagation before enabling HTTPS
- GitHub automatically provisions SSL certificates for custom domains

## 📞 Support

For domain-related issues, contact name.com support.
For email hosting issues, contact your chosen email provider.
For GitHub Pages issues, check [GitHub Pages documentation](https://docs.github.com/en/pages).

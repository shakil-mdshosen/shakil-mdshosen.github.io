# Quick Setup Guide for shakil.live

## 🚀 Your website is ready! Here's how to make it live:

### Step 1: Enable GitHub Pages (2 minutes)
1. Go to your repository: https://github.com/shakil-mdshosen/shakil-mdshosen.github.io
2. Click **Settings** tab
3. Scroll down to **Pages** section
4. Under "Source", select **Deploy from a branch**
5. Choose **main** branch and **/ (root)** folder
6. Click **Save**

### Step 2: Configure DNS at name.com (5 minutes)
Login to your name.com account and add these DNS records:

**For root domain (shakil.live):**
```
Type: A Record
Host: @
Value: 185.199.108.153

Type: A Record  
Host: @
Value: 185.199.109.153

Type: A Record
Host: @  
Value: 185.199.110.153

Type: A Record
Host: @
Value: 185.199.111.153
```

**For www subdomain (optional):**
```
Type: CNAME
Host: www
Value: shakil-mdshosen.github.io
```

### Step 3: Wait for DNS Propagation (24-48 hours)
- DNS changes take time to propagate globally
- You can check status at: https://whatsmydns.net/#A/shakil.live

### Step 4: Enable HTTPS (after DNS works)
1. Return to GitHub Pages settings
2. Check **Enforce HTTPS** (only after domain works)

## 📧 Free Email Setup (Choose One)

### Option A: Cloudflare Email Routing (Recommended - 100% Free Forever)
1. Sign up at https://cloudflare.com (free account)
2. Add domain `shakil.live` to Cloudflare
3. Update nameservers at name.com to Cloudflare's nameservers
4. In Cloudflare dashboard, enable Email Routing
5. Add destination email (your existing email address)
6. Create email addresses like `you@shakil.live`
7. All emails will be forwarded to your existing email
   
**Pros:** Unlimited forwarding, easy setup, reliable, truly free forever

### Option B: ImprovMX (Free Email Forwarding)
1. Sign up at https://improvmx.com
2. Add domain `shakil.live`
3. Add these MX records at name.com:
   ```
   Type: MX, Host: @, Value: mx1.improvmx.com, Priority: 10
   Type: MX, Host: @, Value: mx2.improvmx.com, Priority: 20
   ```
4. Create email aliases that forward to your existing email

### Option C: ForwardEmail.net (Free & Open Source)
1. Sign up at https://forwardemail.net
2. Add domain `shakil.live`
3. Add these DNS records at name.com:
   ```
   Type: MX, Host: @, Value: mx1.forwardemail.net, Priority: 10
   Type: MX, Host: @, Value: mx2.forwardemail.net, Priority: 20
   Type: TXT, Host: @, Value: forward-email=your-email@example.com
   ```

### ⚠️ Note about Zoho Mail
Zoho Mail's free tier for custom domains is no longer widely available for new users. Most free email hosting now requires email forwarding services rather than full mailbox hosting.

## ✅ Final Checklist
- [ ] GitHub Pages enabled
- [ ] DNS records added at name.com
- [ ] Wait 24-48 hours for propagation
- [ ] Test website at https://shakil.live
- [ ] Enable HTTPS in GitHub Pages
- [ ] Choose and setup email hosting
- [ ] Customize website content

## 🆘 Need Help?
- **DNS issues**: Contact name.com support
- **Email issues**: Contact your chosen email provider
- **GitHub Pages**: Check [GitHub Docs](https://docs.github.com/en/pages)

Your website will be live at https://shakil.live once DNS propagates! 🎉
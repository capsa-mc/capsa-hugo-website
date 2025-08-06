# Netlify Deployment Guide

## Deployment Status

Your Hugo website is configured for Netlify deployment with:

✅ **Automatic builds** on every git push  
✅ **Hugo 0.148.2** with extended features  
✅ **Netlify CMS** for content management  
✅ **Deploy previews** for pull requests  
✅ **Form handling** capabilities  
✅ **CDN** and **SSL** included  

## Post-Deployment Checklist

### 1. Update URLs
After deployment, update these files with your actual Netlify URL:

**File: `static/admin/config.yml`**
```yaml
site_url: https://capsa-hugo-website.netlify.app
display_url: https://capsa-hugo-website.netlify.app
logo_url: https://capsa-hugo-website.netlify.app/icons/icon-512x512.png
```

**File: `hugo.toml`**
```toml
baseURL = 'https://capsa-hugo-website.netlify.app'
```

### 2. Enable Content Management

To allow non-technical users to edit content:

1. **Netlify Dashboard** → **Identity** → **Enable Identity**
2. **Settings** → **Registration** → **Invite only**
3. **Services** → **Git Gateway** → **Enable**
4. **Identity** → **Invite users** → Add editor emails

### 3. Content Editor Access

Send this to content editors:

**Admin URL**: `https://capsa-hugo-website.netlify.app/admin/`

**Instructions**:
1. Click the link above
2. Accept the invitation email
3. Set up password
4. Start editing content with the visual interface!

## Custom Domain (Optional)

To use your own domain (e.g., `capsa-mc.org`):

1. **Netlify Dashboard** → **Domain settings**
2. **Add custom domain** → Enter your domain
3. **Configure DNS** → Point to Netlify
4. **SSL** will be automatically provisioned

## Environment Variables

If needed, set environment variables in:
**Netlify Dashboard** → **Site settings** → **Environment variables**

Common variables:
- `HUGO_VERSION` (already set in netlify.toml)
- `HUGO_ENV=production` (already set)

## Branch Deploys

- **Main branch** → Production site
- **Other branches** → Preview URLs
- **Pull requests** → Deploy previews

## Build Performance

Current build settings optimize for:
- **Fast builds** with `--gc` (garbage collection)
- **Optimized output** with `--minify`
- **Git info** for last modified dates

## Monitoring

Monitor your site at:
- **Netlify Analytics** (built-in)
- **Deploy logs** (troubleshooting)
- **Function logs** (if using functions)

## Support

- **Netlify Docs**: https://docs.netlify.com/
- **Hugo Docs**: https://gohugo.io/documentation/
- **Community**: Netlify community forums
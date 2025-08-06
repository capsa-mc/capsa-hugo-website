# Alternative: Deploy via Netlify CLI

## Install Netlify CLI

```bash
npm install -g netlify-cli
```

## Login to Netlify

```bash
netlify login
```

## Deploy from Command Line

### One-time setup:
```bash
# Initialize site
netlify init

# Build site
hugo --gc --minify

# Deploy
netlify deploy --prod --dir=public
```

### Subsequent deploys:
```bash
hugo --gc --minify && netlify deploy --prod --dir=public
```

## Automatic deploys

The recommended approach is still Git-based deployment (automatic) rather than CLI deployment.
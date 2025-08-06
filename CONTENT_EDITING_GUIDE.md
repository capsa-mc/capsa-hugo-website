# Content Editing Guide for CAPSA Website

This guide shows non-technical users how to edit website content. There are 3 ways to edit content:

## Option 1: Netlify CMS (Easiest - Recommended)

**Access the CMS**: Go to `https://capsa-hugo-website.netlify.app/admin/`

This provides a user-friendly interface similar to WordPress:
- ✅ Visual editor with buttons
- ✅ No need to understand markdown
- ✅ Image upload interface
- ✅ Preview before publishing
- ✅ Automatic deployment

**Setup required**: You need to enable Netlify Identity on your site.

## Option 2: GitHub Web Editor (Simple)

This is the basic method using GitHub's built-in editor:

## Quick Start

1. **Go to the repository**: [Your-Repository-URL]
2. **Navigate to content folder**: Click on `content/`
3. **Find the page to edit**:
   - Home page: `_index.md`
   - About page: `about/_index.md` 
   - Blog posts: `blog/[post-name].md`
   - Contact: `contact/_index.md`
   - Resources: `resource/_index.md`
   - Calendar: `calendar/_index.md`
   - Tutoring: `tutoring/_index.md`

## How to Edit a Page

### Step 1: Find Your File
- Click on the `content` folder
- Navigate to the page you want to edit
- Click on the `.md` file

### Step 2: Edit the File
- Click the **pencil icon** (✏️) in the top right
- Make your changes in the text editor
- **Important**: Don't change anything between the `---` lines at the top!

### Step 3: Save Changes
- Scroll to bottom of page
- Add a description of your changes (e.g., "Updated contact information")
- Click **"Commit changes"**
- The website will automatically update in 2-3 minutes!

## Content Structure

### Front Matter (Don't Touch!)
```yaml
---
title: "Page Title"
layout: "page-type"
---
```
**⚠️ Never edit the section between --- lines**

### Page Content
Everything below the second `---` is your content. You can:
- Edit text
- Add/remove bullet points
- Change links
- Update information

## Markdown Formatting

### Headers
```markdown
# Large Header
## Medium Header  
### Small Header
```

### Links
```markdown
[Link Text](https://example.com)
```

### Lists
```markdown
- Item 1
- Item 2
- Item 3
```

### Bold/Italic
```markdown
**bold text**
*italic text*
```

## Adding New Blog Posts

1. Go to `content/blog/`
2. Click **"Add file"** → **"Create new file"**
3. Name it: `your-post-title.md`
4. Add this template:

```markdown
---
title: "Your Post Title"
date: 2025-01-15T10:00:00.000Z
tags:
  - "Tag1"
  - "Tag2"
---

Your blog post content goes here...
```

5. Click **"Commit new file"**

## Common Edits

### Update Contact Information
- File: `content/contact/_index.md`
- Edit the email addresses and phone numbers in the front matter section

### Change Calendar Dates
- File: `content/calendar/_index.md`
- Edit the table with new dates and events

### Update Resource Links
- File: `content/resource/_index.md`
- Add or modify the links in the content section

### Home Page Announcements
- File: `content/_index.md`
- Edit the `description1` field in the front matter

## Need Help?

If you make a mistake:
1. Don't panic! 
2. Contact the website administrator
3. All changes are tracked and can be undone

## Tips
- ✅ Always preview your changes before committing
- ✅ Write clear commit messages
- ✅ Test links to make sure they work
- ❌ Don't edit the front matter (between ---) unless instructed
- ❌ Don't delete files unless sure
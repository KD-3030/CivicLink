# GitHub Repository Rename Instructions

This document provides step-by-step instructions for renaming the GitHub repository from `nextjs-migration` to `CivicLink`.

## Why Rename?

The project has been rebranded to **CivicLink**. While all internal references have been updated (package.json, README, etc.), the GitHub repository itself still uses the old name `nextjs-migration`. Renaming it will provide consistency across the project.

## Steps to Rename the Repository

### 1. Navigate to Repository Settings

1. Go to the repository on GitHub: `https://github.com/KD-3030/nextjs-migration`
2. Click on the **Settings** tab (you need admin access to the repository)

### 2. Rename the Repository

1. Scroll down to the **Repository name** section
2. In the text field, change `nextjs-migration` to `CivicLink` (or `civiclink` if you prefer lowercase)
3. Click the **Rename** button
4. Review the warning message about repository redirects
5. Confirm the rename

### 3. Update Local Clones

After renaming on GitHub, anyone with a local clone needs to update their remote URL:

```bash
# Navigate to your local repository
cd /path/to/your/local/repo

# Update the remote URL
git remote set-url origin https://github.com/KD-3030/CivicLink.git

# Verify the change
git remote -v
```

### 4. Update CI/CD and External Services

If you have any external services connected to this repository, update them with the new URL:

- **CI/CD pipelines** (GitHub Actions, Jenkins, etc.)
- **Webhooks**
- **Issue trackers**
- **Documentation links**
- **README badges** (if any)

### 5. Update README URLs (Optional)

After the repository rename, you may want to update the URLs in README.md:

```markdown
# Old URLs
git clone https://github.com/KD-3030/nextjs-migration.git
cd nextjs-migration

# New URLs (after rename)
git clone https://github.com/KD-3030/CivicLink.git
cd CivicLink
```

## Important Notes

- **Automatic Redirects**: GitHub automatically sets up redirects from the old URL to the new one, so existing clones will continue to work
- **Third-party Integrations**: Some third-party tools may not follow redirects and will need manual updating
- **Links**: Update any documentation, websites, or tools that link to the repository

## What We've Already Done

✅ Updated package.json name from "civiclink-nextjs" to "civiclink"  
✅ Created comprehensive README.md with CivicLink branding  
✅ Updated package-lock.json  
✅ Added project metadata (description, keywords, license)  

## What Still Needs to Be Done

⏳ Rename the GitHub repository from "nextjs-migration" to "CivicLink"  
⏳ Update local git remotes (if needed)  
⏳ Update any CI/CD configurations (if needed)  

## Questions?

If you encounter any issues during the rename process, please refer to the [GitHub documentation on renaming repositories](https://docs.github.com/en/repositories/creating-and-managing-repositories/renaming-a-repository).

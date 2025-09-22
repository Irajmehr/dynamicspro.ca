# LLM Instructions: GitHub Project Upload

## Overview
This guide provides step-by-step instructions for LLMs to upload projects to GitHub repositories.

## Prerequisites
- Project files are ready for upload
- GitHub repository URL is provided by user
- Git is installed on the system

## Step-by-Step Instructions

### 1. Navigate to Project Directory
```powershell
# Navigate to the project root directory
cd "path/to/project"
```

### 2. Initialize Git Repository (if not already initialized)
```powershell
# Check if git is already initialized
git status

# If not a git repository, initialize it
git init
```

### 3. Add All Files to Git
```powershell
# Add all files to staging area
git add .

# Or add specific files/directories
git add src/
git add *.al
git add *.json
```

### 4. Create Initial Commit
```powershell
# Create the first commit with descriptive message
git commit -m "Initial commit: [Project Name] - [Brief Description]"

# Examples:
git commit -m "Initial commit: BDP Approval Hub - Business Central workflow system"
git commit -m "Initial commit: AL Project - All comments removed and code cleaned"
```

### 5. Add Remote Repository
```powershell
# Add the GitHub repository as remote origin
git remote add origin https://github.com/[username]/[repository-name].git

# Example:
git remote add origin https://github.com/UniverseIT-Source-Control/Ranger_Workflow_Approval.git
```

### 6. Set Main Branch (Modern Git Standard)
```powershell
# Rename master branch to main (if needed)
git branch -M main
```

### 7. Push to GitHub
```powershell
# Push to GitHub and set upstream tracking
git push -u origin main

# For subsequent pushes (after initial setup)
git push
```

## Complete Example Workflow

```powershell
# 1. Navigate to project
cd "E:\path\to\project"

# 2. Initialize git (if needed)
git init

# 3. Add all files
git add .

# 4. Commit
git commit -m "Initial commit: [Project Name] - [Description]"

# 5. Add remote
git remote add origin https://github.com/[username]/[repository-name].git

# 6. Set main branch
git branch -M main

# 7. Push to GitHub
git push -u origin main
```

## Error Handling

### If Repository Already Exists
```powershell
# Check if remote already exists
git remote -v

# Remove existing remote if needed
git remote remove origin

# Add new remote
git remote add origin https://github.com/[username]/[repository-name].git
```

### If Authentication Required
- User will be prompted to authenticate in browser
- Follow GitHub authentication prompts
- May need Personal Access Token for private repos

### If Files Are Too Large
```powershell
# Check file sizes
git status

# Add .gitignore to exclude large files
echo "*.app" >> .gitignore
echo "*.app_backup" >> .gitignore
echo "node_modules/" >> .gitignore
```

## Verification Steps

### 1. Check Git Status
```powershell
git status
```

### 2. Verify Remote Connection
```powershell
git remote -v
```

### 3. Check Commit History
```powershell
git log --oneline
```

### 4. Verify Files Are Tracked
```powershell
git ls-files
```

## Best Practices for LLMs

### 1. Always Check Current State
- Verify if git is already initialized
- Check if remote already exists
- Confirm user is in correct directory

### 2. Use Descriptive Commit Messages
- Include project name
- Describe what was uploaded
- Mention key features or changes

### 3. Handle Large Projects
- Consider using .gitignore for large files
- Break large commits into smaller ones if needed
- Monitor upload progress

### 4. Error Recovery
- If push fails, check authentication
- If files are too large, use .gitignore
- If remote exists, remove and re-add

### 5. User Communication
- Inform user of each step
- Show progress and status
- Report any errors clearly
- Confirm successful upload

## Common Commands Reference

```powershell
# Git status
git status

# Add files
git add .

# Commit changes
git commit -m "message"

# Add remote
git remote add origin [url]

# Push to GitHub
git push -u origin main

# Check remotes
git remote -v

# Remove remote
git remote remove origin

# Check branch
git branch

# Rename branch
git branch -M main
```

## Troubleshooting

### Authentication Issues
- Ensure user has GitHub account
- May need Personal Access Token
- Check repository permissions

### Large File Issues
- Use .gitignore to exclude large files
- Consider Git LFS for large files
- Break commits into smaller chunks

### Network Issues
- Check internet connection
- Try again if push fails
- Verify repository URL is correct

## Success Indicators

✅ Repository initialized  
✅ Files added to git  
✅ Initial commit created  
✅ Remote repository added  
✅ Main branch set  
✅ Files pushed to GitHub  
✅ No error messages  
✅ User can access repository on GitHub  

## Final Verification
After upload, verify:
1. Repository exists on GitHub
2. All files are present
3. Commit history is visible
4. User can access the repository
5. No sensitive information was uploaded 
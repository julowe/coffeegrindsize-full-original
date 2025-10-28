# Release Instructions

This document explains how to create a new release with pre-built executables for Windows, macOS, and Linux.

## Automated Release Process

The repository is configured with GitHub Actions to automatically build executables for all three platforms when you create a new release tag.

### Creating a Release

#### Option 1: Using Git Tags (Recommended)

1. Make sure all changes are committed and pushed to the main branch
2. Create and push a new tag:
   ```bash
   git tag v1.0.0
   git push origin v1.0.0
   ```
3. The GitHub Actions workflow will automatically:
   - Build executables for Windows, macOS, and Linux
   - Create a new GitHub Release
   - Attach the executables as release assets

#### Option 2: Manual Workflow Trigger

If you want to build executables without creating a release:

1. Go to the "Actions" tab in the GitHub repository
2. Click on "Build and Release Executables" workflow
3. Click "Run workflow"
4. Select the branch
5. Click "Run workflow"

This will build the executables and make them available as workflow artifacts (downloadable for 90 days), but will NOT create a GitHub release.

## Version Numbering

We recommend following semantic versioning:
- `v1.0.0` - Major release
- `v1.1.0` - Minor release (new features)
- `v1.0.1` - Patch release (bug fixes)

## Release Checklist

Before creating a release:
- [ ] All tests pass
- [ ] Documentation is up to date
- [ ] README.md reflects current features
- [ ] Version number is appropriate
- [ ] CHANGELOG is updated (if you maintain one)

## Post-Release

After creating a release:
1. Verify that all three executables were built successfully
2. Test the executables on each platform if possible
3. Update any external documentation or websites
4. Announce the release to users

## Troubleshooting

If the build fails:
1. Check the Actions tab for error logs
2. Common issues:
   - Missing dependencies in requirements.txt
   - Python version compatibility
   - Platform-specific code issues
3. Fix the issues and push a new tag

## Testing Locally

To test the build process locally before creating a release:

### Linux:
```bash
pip install pyinstaller
pip install -r requirements.txt
pyinstaller --name=coffeegrindsize --windowed --onefile coffeegrindsize.py
```

### Windows:
```powershell
pip install pyinstaller
pip install -r requirements.txt
pyinstaller --name=coffeegrindsize --windowed --onefile coffeegrindsize.py
```

### macOS:
```bash
pip install pyinstaller
pip install -r requirements.txt
pyinstaller --name=coffeegrindsize --windowed --onedir coffeegrindsize.py
```

The executable will be in the `dist/` folder.

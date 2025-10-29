# Getting Started with Automated Builds

This repository is now configured to automatically build standalone executables for Windows, macOS, and Linux!

## What's Been Added

1. **GitHub Actions Workflow** (`.github/workflows/build-release.yml`)
   - Automatically builds executables for all three platforms
   - Can be triggered by pushing a git tag or manually from the Actions tab
   - Creates GitHub releases with executable attachments

2. **Python Dependencies** (`requirements.txt`)
   - Lists all required Python packages
   - Used by the build workflow

3. **Build Configuration** (`.gitignore`)
   - Excludes build artifacts from version control
   - Keeps the repository clean

4. **Documentation**
   - `README.md` - User-facing instructions for downloading and running the app
   - `RELEASE_INSTRUCTIONS.md` - Maintainer guide for creating releases

## Next Steps

### To Test the Workflow Without Creating a Release

1. Go to the repository on GitHub
2. Click on the "Actions" tab
3. Select "Build and Release Executables" workflow
4. Click "Run workflow" button
5. Select your branch and click "Run workflow"
6. Wait for the build to complete (5-10 minutes)
7. Download the artifacts from the workflow run

### To Create Your First Official Release

1. Make sure all your changes are committed and pushed to the main branch
2. Create and push a version tag:
   ```bash
   git checkout main
   git pull
   git tag v1.0.0
   git push origin v1.0.0
   ```
3. The workflow will automatically:
   - Build executables for Windows, macOS, and Linux
   - Create a new GitHub Release at `https://github.com/julowe/coffeegrindsize-full-original/releases`
   - Attach the executables as downloadable assets

### Sharing with Users

Once the release is created, users can:
1. Visit the Releases page
2. Download the appropriate file for their operating system
3. Extract and run the application (no Python installation needed!)

## Troubleshooting

If the build fails:
1. Check the Actions tab for error logs
2. Review `RELEASE_INSTRUCTIONS.md` for common issues
3. Test locally using the commands in `RELEASE_INSTRUCTIONS.md`

## Security

The workflow has been configured with minimal permissions following security best practices:
- Read permissions for building
- Write permissions only for creating releases

---

**Note:** The old `App/` directory with the pre-built macOS app remains in the repository for reference but is not used by the new automated build system.

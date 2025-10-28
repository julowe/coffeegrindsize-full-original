# Coffee Grind Size Analyzer

A GUI application for analyzing coffee grind size distribution from images, developed by Jonathan Gagne.

## Download Standalone Executables

Pre-built standalone executables are available for Windows, macOS, and Linux. No Python installation required!

### Latest Release

Visit the [Releases page](https://github.com/julowe/coffeegrindsize-full-original/releases) to download the latest version for your operating system.

**Note:** If no releases are available yet, the repository owner can create one by pushing a git tag (e.g., `v1.0.0`) or by manually triggering the "Build and Release Executables" workflow from the Actions tab.

### Installation Instructions

#### Windows
1. Download `coffeegrindsize-windows.zip` from the latest release
2. Extract the ZIP file to a folder of your choice
3. Double-click `coffeegrindsize.exe` to run the application

#### macOS
1. Download `coffeegrindsize-macos.zip` from the latest release
2. Extract the ZIP file
3. Move `coffeegrindsize.app` to your Applications folder (optional)
4. Right-click (or Control-click) on `coffeegrindsize.app` and select "Open"
5. Click "Open" in the security dialog that appears (first time only)

**Note for macOS users:** You may need to allow the app in System Preferences > Security & Privacy if you see a security warning.

#### Linux
1. Download `coffeegrindsize-linux.tar.gz` from the latest release
2. Extract the archive: `tar -xzf coffeegrindsize-linux.tar.gz`
3. Make the file executable: `chmod +x coffeegrindsize`
4. Run the application: `./coffeegrindsize`

## Running from Source

If you prefer to run from source code:

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### Installation
1. Clone this repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the application:
   ```bash
   python coffeegrindsize.py
   ```

## Usage

1. **Open Image**: Load an image of coffee grounds
2. **Select Reference Object**: Draw a line on a reference object of known size (e.g., a coin)
3. **Select Analysis Region**: Draw a polygon around the coffee grounds to analyze
4. **Threshold Image**: Apply thresholding to identify coffee particles
5. **Launch Particle Detection**: Analyze the particles in the image
6. **Create Histogram**: Generate distribution histograms
7. **Save Data**: Export results to CSV files

For detailed instructions, click the "Help" button in the application or visit the [Coffee Ad Astra Blog](https://coffeeadastra.com).

## Additional Resources

For alternative OS X and Windows installation packages, see this GitHub repo by Chris Saterlee:
https://github.com/csatt/coffeegrindsize/releases/tag/v1.0.0

Thanks a lot Chris!

## Credits

Application developed by **Jonathan Gagne**

## License

See LICENSE file for details.

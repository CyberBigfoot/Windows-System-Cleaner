# Windows-System-Cleaner

[![Support on Buy Me a Coffee](https://img.shields.io/badge/Support-Buy%20Me%20a%20Coffee-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/onlycyber)

A comprehensive GUI application for Windows system maintenance, optimization, and advanced drive analysis. This tool provides an easy-to-use interface for performing various system cleaning, maintenance, reporting tasks, and health monitoring.

## New in Version 1.3

- **Enhanced Layout**: Transitioned to a clean, equal-width, two-column dashboard maximizing vertical space for faster tool discovery.
- **MiniDump Analyzer**: Seamlessly integrates NirSoft's BlueScreenView to quickly diagnose BSOD (Blue Screen of Death) crash dumps.
- **Deep Network Stack Remediation**: A comprehensive one-click fix for complex network connection issues, resetting everything from winsock to IP configurations and flushing DNS.
- **Sysinternals Integration**: Direct, one-click access to Microsoft's legendary Sysinternals tools—specifically **Autoruns** (startup management) and **Process Explorer** (advanced task manager).
- **Custom Application Icon**: Added a sleek custom icon to replace the default aesthetic, visible in both the UI banner and the executable file.

## Features

### App Installer
-   **Massive Database**: 350+ tools including Browsers, Development Environments, Multimedia, and Communications.
-   **Categorized Browsing**: Simplified navigation with a categorized sidebar.
-   **Integrated Search**: Quickly find the tools you need.
-   **Winget Backend**: Utilizes Microsoft's official package manager for secure, fast installations.

### StorageSense and Drive Health
-   **Advanced Disk Visualization**: Interactive directory tree and file list with size visualization.
-   **Drive Health Monitoring**: Real-time S.M.A.R.T. data analysis including:
    -   Health Status (Healthy/Warning/Critical)
    -   Temperature and Wearout levels
    -   Performance stats (IOPS, Latency)
-   **Large File Finder**: Color-coded highlights for large files to easily identify space hogs.
-   **Integrated Management**: Open file locations or delete files directly from the analyzer.

### Core System Tasks
-   **Clean Temporary Files**: Removes temporary files from system directories to free up space.
-   **Deep Disk Cleanup**: Automates Windows Disk Cleanup with comprehensive options.
-   **Optimize Virtual Memory**: Detects RAM and sets the optimal Page File size (2x RAM) for performance.
-   **Disable Fast Startup**: Ensures complete system shutdowns to prevent uptime-related issues.
-   **Repair System**: Runs standard Windows repairs (sfc and DISM).

### System Optimization and Maintenance
-   **Performance Adjustments**: Applies tweaks to disable unnecessary visual effects and features.
-   **App Settings Manager**: Control background apps and startup services.
-   **Update Services**: Update installed apps via Winget and check for Windows/Firmware updates.

### Network and Connectivity
-   **Deep Network Stack Remediation**: Full reset of network configurations.
-   **Flush DNS and Renew IP**: Clears DNS cache and refreshes network identity.
-   **Detailed Network Config**: Comprehensive adapter and IP information.
-   **Fast DNS Switcher**: One-click switch to high-performance providers like Cloudflare or Google.

### Advanced IT Diagnostic Tools
-   **MiniDump Analyzer**: Open BSOD crash dumps using built-in BlueScreenView logic.
-   **Sysinternals Launchers**: Directly open Autoruns and Process Explorer.
-   **Detailed Reporting**: Generate in-depth HTML system reports covering hardware, software, and security status.
-   **Chris Titus Utility**: Integrated launcher for the Chris Titus Tech Windows Utility.

## Personalization

The application supports dynamic UI scaling via the View menu, and multiple themes to match your workspace:
- Light
- Dark
- Cyberpunk (Neon)
- Ocean (Blue/Teal)
- Sunset (Orange/Purple)
- Forest (Green)

Switch themes instantly via the **View > Theme** menu.

## Installation

### Method 1: Standalone Executable (Recommended)
You can simply run the compiled `Windows-System-Cleaner.exe` directly on any Windows 10/11 machine. No Python installation or dependencies are required.

### Method 2: Running from Source
**Prerequisites**
-   **OS**: Windows 10/11 (64-bit).
-   **Python**: Version 3.8 or higher.

**Dependencies**
Install the required Python packages:
```bash
pip install wmi requests beautifulsoup4 psutil customtkinter
```

**Running the Application**
1.  Open Command Prompt or PowerShell as **Administrator** (required for system tasks).
2.  Navigate to the application directory.
3.  Run the main script:
    ```bash
    python Windows-System-Cleaner.py
    ```

## Usage

### The Interface
The dashboard is split into two primary, equal-width columns to maximize vertical space:
-   **Left Column**: Core system maintenance, optimization tasks, app settings, and update management.
-   **Right Column**: Additional advanced tasks, network remediation, reporting functionalities, and IT diagnostic tool launchers.

### Using the App Installer
1.  Navigate to the App Installer tab or use the search bar within the UI.
2.  Select the apps you wish to install across various categories.
3.  Click "Install Selected" to begin the batch process.

## Security and Safety
-   **Admin Required**: Most features modify system settings natively and require elevated permissions.
-   **Input Sanitization**: Commands are sanitized to prevent injection or path traversal.
-   **Safe Defaults**: Destructive actions require user confirmation.

## License
This project is licensed under the MIT License.

## Disclaimer
This software provides powerful system tools. Always backup important data before running system repairs or large-scale file deletions. Use at your own risk.

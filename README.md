# Windows System Cleaner

[![Support on Buy Me a Coffee](https://img.shields.io/badge/Support-Buy%20Me%20a%20Coffee-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/onlycyber)

A comprehensive GUI application for Windows system maintenance, optimization, and advanced drive analysis. This tool provides an easy-to-use interface for performing various system cleaning, maintenance, reporting tasks, and health monitoring.

## New in Version 1.2

-   **Rebranding**: Full transition to "Windows System Cleaner" for a professional, consistent experience.
-   **Integrated App Installer**: Over 350 popular applications available for batch installation via Winget.
-   **Fun Themes**: Support for Cyberpunk, Ocean, Sunset, and Forest themes alongside Light and Dark modes.
-   **Virtual Memory Optimizer**: Automatic RAM-to-PageFile calculation and optimization.
-   **Dynamic UI Scaling**: Adjustable font sizes across the entire application.

## Features

### App Installer (v1.2)
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
-   **Flush DNS and Renew IP**: Clears DNS cache and refreshes network identity.
-   **Detailed Network Config**: Comprehensive adapter and IP information.
-   **Fast DNS Switcher**: One-click switch to high-performance providers like Cloudflare or Google.

### Reporting and Utilities
-   **PC System Report**: Generates a detailed HTML report of hardware, software, and security status.
-   **Chris Titus Utility**: Integrated launcher for the Chris Titus Tech Windows Utility.

## Personalization

The application now supports several themes to match your workspace:
- Light
- Dark
- Cyberpunk (Neon)
- Ocean (Blue/Teal)
- Sunset (Orange/Purple)
- Forest (Green)

Switch themes instantly via the **View > Theme** menu.

## Installation

### Prerequisites
-   **OS**: Windows 10/11 (64-bit).
-   **Python**: Version 3.8 or higher.
-   **Privileges**: Administrator rights are required for most operations.

### Dependencies
Install the required Python packages:
```bash
pip install wmi requests beautifulsoup4 psutil customtkinter
```

### Running the Application
1.  Open Command Prompt or PowerShell as **Administrator**.
2.  Navigate to the application directory.
3.  Run the main script:
    ```bash
    python main.py
    ```

## Usage

### The Interface
The dashboard is split into three primary columns:
-   **Left Column (Core System Tasks)**: Essential maintenance and optimization.
-   **Center (App Settings)**: Management for apps, background services, and updates.
-   **Right Column (Additional Tasks)**: Advanced utilities, reporting, and the StorageSense launcher.

### Using the App Installer
1.  Navigate to the App Installer tab (if launched separately) or use the search bar within the UI.
2.  Select the apps you wish to install.
3.  Click "Install Selected" to begin the batch process.

## Security and Safety
-   **Admin Required**: Most features modify system settings and require elevated permissions.
-   **Input Sanitization**: Commands are sanitized to prevent injection or path traversal.
-   **Safe Defaults**: Destructive actions require user confirmation.

## License
This project is licensed under the MIT License.

## Disclaimer
This software provides powerful system tools. Always backup important data before running system repairs or large-scale file deletions. Use at your own risk.

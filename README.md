# EAWTECH-Tool (Windows System Cleaner)

A comprehensive GUI application for Windows system maintenance, optimization, and advanced drive analysis. This tool provides an easy-to-use interface for performing various system cleaning, maintenance, reporting tasks, and health monitoring.

## Features

### 🔍 StorageSense & Drive Health (NEW)
-   **Advanced Disk Visualization**: Interactive directory tree and file list with size visualization.
-   **Drive Health Monitoring**: Real-time S.M.A.R.T. data analysis including:
    -   Health Status (Healthy/Warning/Critical)
    -   Temperature & Wearout levels
    -   Power On Hours & Cycle counts
    -   Read/Write Error rates
    -   Performance stats (IOPS, Latency)
-   **Large File Finder**: Color-coded highlights for large files to easily identify space hogs.
-   **File Type Hints**: Smart descriptions for known file types (e.g., "safe to delete" hints for temp files).
-   **Integrated Management**: Open file locations or delete files directly from the analyzer.

### 🛠️ Core System Tasks
-   **Clean Temporary Files**: Removes temporary files from system directories to free up space.
-   **Deep Disk Cleanup**: Automates Windows Disk Cleanup with comprehensive options.
-   **Disable Fast Startup**: Disables Fast Startup to ensure complete system shutdowns (fixes many uptime issues).
-   **Repair System**: Runs standard Windows repairs (`sfc /scannow` and DISM).
-   **Schedule CHKDSK**: Schedules a disk check for the next reboot.

### 🚀 System Optimization & Maintenance
-   **Performance Adjustments**: Applies tweaks for better performance (disables transparency, game bar, etc.).
-   **Stop Background Apps**: Prevents unnecessary apps from running in the background.
-   **Disable Startup Apps**: Optimizes boot time by disabling non-essential startup programs (excludes OneDrive).
-   **Update Installed Apps**: Update specific or all installed applications using `winget`.
-   **Windows Updates**: Checks for and installs available Windows system updates.
-   **Firmware Updates**: Automatically checks for Dell, HP, or Lenovo firmware updates.

### 🌐 Network & Connectivity
-   **Flush DNS & Renew IP**: Clears DNS cache and requests a new IP address.
-   **Detailed Network Config**: Displays comprehensive IP and network adapter information.
-   **Fast DNS Switcher**: One-click switch to high-performance DNS providers (Cloudflare 1.1.1.1 / Google 8.8.8.8).

### 📊 Reporting & Utilities
-   **PC System Report**: Generates a detailed HTML report of your system hardware and software (similar to Belarc).
-   **AutoPilot CSV**: Exports hardware hash for Windows AutoPilot deployment.
-   **Chris Titus Utility**: Integrated launcher for the popular Chris Titus Tech Windows Utility.

## Installation

### Prerequisites
-   **OS**: Windows 10/11 (64-bit) recommended.
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
The application is divided into logical sections:
-   **Left Column (Core & Apps)**: Essential cleaning tasks and application management.
-   **Right Column (Additional Tasks)**: Network tools, reporting, and the **StorageSense** launcher.
-   **Bottom**: Real-time activity log showing operation status and results.

### Using StorageSense
1.  Check the **"StorageSence (Drive Scanner)"** box in the "Additional Tasks" section.
2.  Click **"Run Selected Tasks"**.
3.  A new window will open. Click **"Select Drive"** to choose a target.
4.  Click **"Start Scan"** to begin analyzing.
5.  Click **"Drive Health"** at the bottom to view detailed S.M.A.R.T. statistics.

### Command Line Options
You can also run specific tasks directly via CLI arguments:
```bash
python main.py --clean-temp 1 --disk-cleanup 1
```
Use `python main.py --help` to see all available command-line flags.

## Security & Safety
-   **Admin Required**: Most features modify system settings and require elevated permissions.
-   **Safe Defaults**: Destructive actions (like file deletion) require user confirmation.
-   **Sanitization**: Input paths and commands are sanitized to prevent execution errors.

## License
This project is licensed under the MIT License.

## Disclaimer
This software provides powerful system tools. **Always backup important data** before running system repairs or large-scale file deletions. Use at your own risk.

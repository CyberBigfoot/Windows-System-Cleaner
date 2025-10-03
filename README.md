# Windows System Cleaner

A comprehensive GUI application for Windows system maintenance and optimization. This tool provides an easy-to-use interface for performing various system cleaning, maintenance, and reporting tasks.

## Features

- **Core System Tasks**
  - Clean temporary files from system directories
  - Run Windows Disk Cleanup with all options
  - Disable Windows Fast Startup
  - Repair system files using SFC and DISM
  - Schedule CHKDSK to run on next reboot

- **System Updates & Maintenance**
  - Check and install Windows updates
  - Update installed applications using Windows Package Manager (winget)
  - Check and install device firmware updates (Dell, HP, Lenovo)

- **Network & Connectivity**
  - Flush DNS and renew IP address
  - Display detailed IP configuration
  - Change DNS servers to 1.1.1.1 and 8.8.8.8

- **System Optimization**
  - Windows performance adjustments (disable Focus Assist, transparency effects, Game Bar)
  - Stop background applications
  - Disable startup applications (except OneDrive)

- **Reporting & Utilities**
  - Generate comprehensive PC system report (similar to Belarc Advisor)
  - Create AutoPilot CSV for Windows deployment
  - Run Chris Titus Windows Utility

## Installation

### Prerequisites

- Windows 7/8/10/11 (64-bit)
- Python 3.8 or higher
- Administrator privileges (required for most features)

### Dependencies

Install the required Python packages:

```bash
pip install wmi requests beautifulsoup4 psutil
```

### Running the Application

1. Download the `system_cleaner.py` file
2. Open Command Prompt or PowerShell as Administrator
3. Navigate to the directory containing the file
4. Run the application:

```bash
python system_cleaner.py
```

## Usage

### GUI Interface

The application provides a user-friendly graphical interface with the following sections:

1. **Core System Tasks** (left column)
   - Select tasks by checking the boxes
   - Tasks requiring admin privileges are marked with "A"
   - Tasks available to standard users are marked with "U"

2. **App Settings** (left column)
   - Configure application-related settings
   - Stop background apps
   - Disable startup apps
   - Update installed apps

3. **Additional System Tasks** (right column)
   - Advanced system maintenance options
   - Network configuration tools
   - Reporting utilities

4. **Activity Log**
   - Real-time logging of all operations
   - Timestamped entries for each action

### Command Line Options

You can also run specific tasks directly from the command line:

```bash
python system_cleaner.py --clean-temp 1 --disk-cleanup 1 --disable-fast-startup 1
```

Available options:
- `--clean-temp` (0/1): Clean temporary files
- `--disk-cleanup` (0/1): Run disk cleanup
- `--disable-fast-startup` (0/1): Disable fast startup
- `--update-apps` (0/1): Update installed apps
- `--windows-updates` (0/1): Install Windows updates
- `--device-firmware` (0/1): Update device firmware
- `--repair-system` (0/1): Repair system files
- `--chk-dsk` (0/1): Schedule CHKDSK
- `--windows-adjustments` (0/1): Apply Windows adjustments
- `--flush-dns` (0/1): Flush DNS and renew IP
- `--ipconfig-all` (0/1): Display IP configuration
- `--change-dns` (0/1): Change DNS servers
- `--autopilot-csv` (0/1): Create AutoPilot CSV
- `--pc-report` (0/1): Generate PC report
- `--chris-titus-utility` (0/1): Run Chris Titus Utility
- `--stop-background-apps` (0/1): Stop background apps
- `--disable-startup-apps` (0/1): Disable startup apps

### Customization

- **Theme Toggle**: Switch between light and dark themes using the View menu
- **Font Size**: Adjust font size (Small, Medium, Large, Extra Large) via the Change Font Size menu

## Security Considerations

This application performs system-level operations and requires administrator privileges for most features. The following security measures have been implemented:

1. **Path Sanitization**: All file paths are sanitized to prevent path traversal attacks
2. **Command Argument Sanitization**: Command line arguments are sanitized to prevent injection attacks
3. **Registry Validation**: Registry key paths are validated against allowed patterns
4. **Secure Execution**: PowerShell commands are executed with limited privileges where possible
5. **Error Handling**: Comprehensive error handling prevents information leakage

**Important**: Only run this application if you trust the source and understand the operations being performed. Always review the changes before applying them to your system.

## Troubleshooting

### Administrator Privileges

Most features require administrator privileges. If you encounter permission errors:

1. Right-click on Command Prompt or PowerShell
2. Select "Run as administrator"
3. Navigate to the application directory
4. Run the application again

### Common Issues

- **Windows Updates**: Some updates may require a system reboot to complete
- **CHKDSK**: This operation will run on the next system reboot and may take a long time
- **Firmware Updates**: Manufacturer-specific utilities may need to be installed separately
- **PC Report Generation**: This process may take several minutes to complete

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Disclaimer

This software is provided "as is" without warranty of any kind. Use at your own risk. The authors are not responsible for any damage to your system that may result from using this software. Always back up your important data before performing system maintenance operations.

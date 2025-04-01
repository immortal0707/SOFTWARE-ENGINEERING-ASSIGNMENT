# SOFTWARE-ENGINEERING-ASSIGNMENT

# Implementing Software Design Principles Using Linux Utilities and Shell Scripting

## Introduction
This project demonstrates the application of software design principles in a Linux-based automation system. It implements an **Automated File Organization System** that sorts and organizes files in a specified directory based on their type, reducing clutter and improving accessibility.

## Features
- **Abstraction:** Separate scripts for file scanning, moving, logging, and scheduling.
- **Encapsulation:** Functional scripts with specific roles.
- **Modularity:** Independent script execution for better maintainability.
- **Cohesion & Coupling:** High cohesion in individual scripts with low coupling for flexibility.

## Software Architecture
- **Scripts Included:**
  - `file_scanner.sh`: Scans directories and categorizes files.
  - `file_mover.sh`: Moves files to designated folders.
  - `setup.sh`: Configures the system for execution.
  - `logger.sh`: Logs all activities and errors.
- **Data Flow Diagram (DFD)** (Refer to documentation)
- **Class Diagram (for Python-based implementation)**
- **Deployment Design:** Uses `cron` for scheduling automation.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/linux-shell-scripting-design.git
   ```
2. Navigate to the project directory:
   ```bash
   cd linux-shell-scripting-design
   ```
3. Set execution permissions:
   ```bash
   chmod +x *.sh
   ```
4. Configure the cron job:
   ```bash
   crontab -e
   ```
   Add the following line to automate execution every 10 minutes:
   ```bash
   */10 * * * * /path/to/file_scanner.sh
   ```
5. Verify logs:
   ```bash
   cat $HOME/file_organizer.log
   ```

## Performance Evaluation
- Used `time ./file_scanner.sh` to measure execution time.
- Used `top`, `htop`, and `vmstat` for system performance monitoring.

## Risk Management
| Risk Type | Issue | Solution |
|-----------|-----------------|----------------|
| Technical | Incorrect permissions | Run `chmod +x *.sh` |
| Operational | Files moved incorrectly | Test in a sample directory first |
| Security | Unauthorized script execution | Restrict execution permissions |

## License
This project is licensed under the MIT License.

## Contributing
Feel free to fork this repository and submit pull requests with improvements!

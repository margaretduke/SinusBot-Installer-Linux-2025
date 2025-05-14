# SinusBot Installer for Linux 2025

## Officially supported Linux distributions
- Debian 11+
- Ubuntu 22.04+

## Installation
```bash
bash <(wget --no-check-certificate -O - 'https://raw.githubusercontent.com/margaretduke/SinusBot-Installer-Linux-2025/main/sinusbot_installer.sh')
```
This command basically downloads the latest version of the installer-script and executes it via the bash.

## Features
- Install the SinusBot to a selected folder
  - Automatic = /opt/sinusbot
  - or own dir
- Update the SinusBot and youtube-dlp
- Reset the password
- Uninstall the bot

The following tasks will be done:

- Checks if the linux distribution is supported
- Installs the latest supported version of the teamspeak client
- Installs all the necessary dependencies
- Creates a separated user
- Installs the latest SinusBot version
- Installs youtube-dlp
- Adds a cronjob for daily youtube-dlp update
- Sets all the file permissions correctly
- Generates startup files:
  - systemd file => service sinusbot {start|stop|restart|status}
  - init.d => /etc/init.d/sinusbot {start|stop|restart}
- Removes all temporary files
- Starts the SinusBot after installation

The duration of the installation process depends on your system (how many packages need to be updated, internet connection, processing power) but typically takes about one to five minutes.

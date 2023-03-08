# Aria2 one-click installation management script enhanced version

[![LICENSE](https://img.shields.io/github/license/P3TERX/aria2.sh?style=flat-square)](https://github.com/P3TERX/aria2.sh/blob/master/LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/P3TERX/aria2.sh.svg?style=flat-square&label=Stars&logo=github)](https://github.com/P3TERX/aria2.sh/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/P3TERX/aria2.sh.svg?style=flat-square&label=Forks&logo=github)](https://github.com/P3TERX/aria2.sh/fork)

Aria2 is currently the most powerful all-round download tool, it supports BT, magnet, HTTP, FTP and other download protocols, and is often used as a server for offline downloads. The Aria2 one-click installation management script is one of the most well-known script works of the Toyo boss. On November 14, 2018, the Toyo boss suddenly lost contact due to unknown reasons. Since the blogger likes Aria2 very much, he has taken over this project since December 7, 2018, and has optimized a lot of functions and details, and has continued to maintain it until now. The enhanced version of the script integrates [Aria2 Perfect Configuration](https://github.com/P3TERX/aria2.conf). This configuration scheme will be downloaded during the installation of Aria2. This scheme includes configuration files and additional function scripts and other files are used to enhance and expand Aria2 functions, improve the download speed and user experience of Aria2, and solve the problems encountered in the use of Aria2 such as no BT download speed, disk space occupied by residual files, task loss, and repeated downloads.

## Features

- Use [Aria2 Perfect Configuration](https://github.com/P3TERX/aria2.conf) scheme
     * BT download rate is high and fast
     * No loss of task progress and no repeated downloads after restarting
     * Delete tasks that are being downloaded and automatically delete unfinished files
     * Download errors automatically delete unfinished files
     * Automatically delete the control file (`.aria2` extension file) after the download is complete
     * After the download is complete, the torrent file (`.torrent` extension file) will be automatically deleted
     * Automatically delete the empty directory after the download is complete
     * Automatically clear junk files after BT download is complete (file type filtering function)
     * Automatically clear small files after BT download is complete (file size filtering function)
     * It has a certain anti-copyright complaint and anti-thunder blood-sucking effect
     * Better PT download support

- Use the latest statically compiled binaries from the [Aria2 Pro Core](https://github.com/P3TERX/Aria2-Pro-Core) project
     - Multi-platform: `amd64`, `i386`, `arm64`, `armhf`
     - Full-featured: `Async DNS`, `BitTorrent`, `Firefox3 Cookie`, `GZip`, `HTTPS`, `Message Digest`, `Metalink`, `XML-RPC`, `SFTP`
     - There is no upper limit to the maximum number of threads on a single server (the limit on the number of threads has been cracked)
     - Anti-loss thread optimization
     - The latest dependent library, the download is more secure, stable and fast
     - Continuously update the latest version

- Support linkage with [RCLONE](https://rclone.org/), more extended functions and gameplay:
     - [Offline download of OneDrive, Google Drive, etc.](https://p3terx.com/archives/offline-download-of-onedrive-gdrive.html)
     - [Baidu netdisk transfer to OneDrive, Google Drive and other network drives](https://p3terx.com/archives/baidunetdisk-transfer-to-onedrive-and-google-drive.html)

- Supports new generation Internet Protocol IPv6
- Regularly update the BT tracker list (no need to restart)

## project address

https://github.com/P3TERX/aria2.sh

Please click `star` to support the project, so that more people can discover, use and benefit. Your support is my driving force for continuous development and maintenance.

## System Requirements

CentOS 6+ / Debian 6+ / Ubuntu 14.04+

## Architecture support

x86_64/i386/ARM64/ARM32v7/ARM32v6

## Instructions for use

* In order to ensure normal use, please install the basic components `wget`, `curl`, `ca-certificates` first, taking Debian as an example:
```
apt install wget curl ca-certificates
```

* Download script
```
wget -N git.io/aria2.sh && chmod +x aria2.sh
```

* Run the script
```
./aria2.sh
```

* Choose the option you want to execute
```
  Aria2 one-click installation management script enhanced version [v2.7.4] by P3TERX.COM
 
   0. Upgrade script
  ————————————————————————
   1. Install Aria2
   2. Update Aria2
   3. Uninstall Aria2
  ————————————————————————
   4. Start Aria2
   5. Stop Aria2
   6. Restart Aria2
  ————————————————————————
   7. Modify the configuration
   8. View configuration
   9. View log
  10. Clear the log
  ————————————————————————
  11. Manually update BT-Tracker
  12. Automatically update BT-Tracker
  ————————————————————————

  Aria2 Status: Installed | Started

  Auto-Update BT-Tracker: Enabled

  Please enter a number [0-12]:
```

## Other operations

Start: `/etc/init.d/aria2 start` | `service aria2 start`

Stop: `/etc/init.d/aria2 stop` | `service aria2 stop`

Restart: `/etc/init.d/aria2 restart` | `service aria2 restart`

View status: `/etc/init.d/aria2 status` | `service aria2 status`

Configuration file path: `/root/.aria2c/aria2.conf` (the configuration file has Chinese comments, if there is a problem with the language setting, it will cause Chinese garbled characters)

Default download directory: `/root/downloads`

RPC key: Randomly generated, you can use option `7. Modify configuration file` to customize

## How to deal with problems

Read the [FAQ](https://p3terx.com/archives/aria2_perfect_config-faq.html) before asking any questions. You can also join the [Aria2 TG group](https://t.me/Aria2c) and small Partners discuss together. Pay attention to the way of asking questions and provide useful information. Before asking questions, it is recommended to study "[The Wisdom of Asking Questions](https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way/blob/master /README-zh_CN.md)", which can better help you solve problems and save time. Questions like "Why doesn't it work?", "So can you help me?" No one should know.

## Update log

Update push: [Aria2 Channel](https://t.me/Aria2_Channel)

### 2020-12-26 v2.7.4 Final

> **NOTICE:** Due to the historical baggage of the script code, this will be the last maintenance update. In the future, a completely new script may be written instead.

- Replaced Aria2 binaries download link
- Fix some bugs

<details>
<summary>History</summary>

### 2020-08-15 v2.7.0

- Added AriaNg link function

### 2020-08-09 v2.6.2

- Modify resource download link
- Optimize IP detection interface

### 2020-07-12 v2.6.0

- Adapt to the new version [Aria2 Perfect Configuration](https://github.com/P3TERX/aria2.conf)
- Remove Aria2 version selection function

### 2020-06-27 v2.5.3

- Synchronize Aria2 perfect configuration filename changes
- Optimization of installation process
- fix bugs

### 2020-05-21 v2.5.0

- Solve the problem that `aria2c` cannot be downloaded directly under CLI
- Modify the configuration directory to `/root/.aria2c`
- Modify the download directory to `/root/downloads`

### 2020-05-20 v2.4.5

- Added auto-update BT Tracker status display
- Improved script upgrade strategy
- Optimize copy details
- Fix some historical bugs

### 2020-05-17 v2.3.0

- Optimize the installation experience in the "LAN" environment in mainland China

### 2020-05-09 v2.2.5

- Added IPv6 address detection function
- Optimize firewall settings and automatically open necessary ports.
- Fix some historical bugs

### 2020-04-14 v2.2.1

- Optimize the BT Tracker list update strategy, without restarting (**automatically update BT Tracker** function needs to be reset)
- Optimize code details and fix some historical bugs

### 2020-02-18 v2.2.0

- Replace the download source of statically compiled binaries ([P3TERX/aria2-builder](https://github.com/P3TERX/aria2-builder))
- Adapt to ARM64, ARM32v7, ARM32v6 architecture.
- Optimize copy details.

### 2020-02-17 v2.1.0

- Adapt to the new version [Aria2 Perfect Configuration](https://github.com/P3TERX/aria2.conf)
- Separate trackers update functionality
- Optimize functions, improve details, and fix some bugs

### 2019-11-23 v2.0.8

- Modify Trackers source ([XIU2/TrackersListCollection](https://github.com/XIU2/TrackersListCollection))

### 2019-10-12 v2.0.7

- Fixed the bug that the Aria2 version was downloaded incorrectly and could not be started because the CPU architecture was not obtained when the Aria2 version was updated

### 2019-09-30 v2.0.6

- Get DHT (IPv6) file

### 2019-06-08 v2.0.5

- Added clear log function
- Adjust some copywriting

### 2018-12-25 v2.0.4

- Optimized adjustments

### 2018-12-24 v2.0.3

- Add reset/update Aria2 perfect configuration option
- Optimized to modify the download path in the additional function script synchronously when modifying the download path of the configuration file

### 2018-12-8 v2.0.2

- Fix the bug that the additional function script does not have execution permission

### 2018-12-7 v2.0.1

- Fix the bug that the prompt does not exist when setting the download folder
- Unlock Update BT-Tracker Servers option

### 2018-12-7 v2.0.0α

- Integrate [Aria2 Perfect Configuration](https://github.com/P3TERX/aria2_perfect_config)

### 2018-10-18 v1.1.10

- Taken from [a Doubi script written by Doubi](https://github.com/P3TERX/doubi_backup)
- Thanks Toyo Boss

</details>

## Lisence
[MIT](https://github.com/P3TERX/aria2.sh/blob/master/LICENSE) © Toyo x P3TERX

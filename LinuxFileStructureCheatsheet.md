| **Directory** | **Purpose**                     | **Examples**                            |
| ------------- | ------------------------------- | --------------------------------------- |
| `/`           | Root of the filesystem          | Everything starts here                  |
| `/bin`        | Essential command binaries      | `ls`, `cp`, `rm`, `cat`                 |
| `/sbin`       | System binaries for admin       | `reboot`, `iptables`, `ifconfig`        |
| `/etc`        | System-wide configuration files | `/etc/passwd`, `/etc/ssh/sshd_config`   |
| `/home`       | User home directories           | `/home/you/`, `/home/jane/.bashrc`      |
| `/root`       | Root user’s home directory      | Only accessible to root                 |
| `/usr/bin`    | User-level programs             | `python`, `gcc`, `git`, `curl`          |
| `/usr/sbin`   | Admin tools for users           | `apache2`, `nginx`, `sshd`              |
| `/usr/lib`    | Libraries for binaries          | `/usr/lib/libc.so`                      |
| `/usr/local/` | Locally installed software      | Compiled software from source           |
| `/opt/`       | Optional third-party software   | `/opt/google/chrome/`                   |
| `/var/log/`   | Log files                       | `syslog`, `auth.log`, `nginx/error.log` |
| `/var/spool/` | Queued tasks (like mail/print)  | `cron`, `cups`, `mail`                  |
| `/tmp/`       | Temporary files                 | Deleted at reboot                       |
| `/dev/`       | Device files                    | `sda`, `null`, `tty`                    |
| `/mnt/`       | Temporary mounts                | Mounting USB drives                     |
| `/media/`     | Auto-mounted external devices   | USB, CD-ROM                             |
| `/proc/`      | Virtual system info             | `/proc/cpuinfo`, `/proc/meminfo`        |
| `/sys/`       | Kernel/device info              | Used by tools like `udev`               |





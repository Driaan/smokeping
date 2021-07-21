# SmokePing one-click script

[SmokePing](https://oss.oetiker.ch/smokeping) is an open source software
developed by RRDtool author Tobi Oetiker to monitor network status and
stability. After the script is installed, SmokePing will periodically send TCP
packets to the target, and measure and record the return value. The RRDtool
drawing program graphically displays the network delay, jitter and packet loss
rate in each period of time, helping us to be more clear , A more intuitive
understanding of the server's network status.

This script will make SmokePing run on Nginx. In order to coexist with other web
services that may exist, ports 9007 and 9008 are required. Please make sure that
they are not occupied.

Currently supported Linux distributions:

```
Debian 9+
Ubuntu 18+
CentOS 7+
Amazon Linux 2
Oracle Linux 7+
```

## Installation

```
bash -c "$(curl -L https://github.com/Driaan/smokeping/raw/main/main.sh)"
```

If `command not found` appears, please execute `apt-get install curl -y` or
`yum install curl -y`.

## Configuration

The script automatically configures SmokePing and can be modified as needed. The
main SmokePing configuration file (including the target node) is
`/usr/local/smokeping/etc/config`. For the structure and modification of this
file, please refer to the relevant tutorial, and attach
[example](https://oss.oetiker.ch /smokeping/doc/smokeping_examples.en.html).

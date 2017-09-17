# VirtualHost manager for Apache 2.4.18

Since I test various opensource selfhosted apps on my virtual machine I decided to create a small script written in bash that helps me to configure initial settings.

I've tested it on Ubuntu 14.04 LTS, it should work also for earlier version and with different Apache versione, please let me know. 

I might update the script for backward and future compatibility. 

This release it is only a prototype.

## What does the script do?
This script basically lets you create, delete or list all available apache VirtualHost.

## Syntax

```
Usage: vhost-manager -vh  [-a ACTION ] [-e EMAIL] [-w DOMAIN_NAME] [-n VHOST_NAME] [-u USER_NAME] [-d DIR_NAME] [-m NOT_MAKE_DIR]
	
        -a                      create, delete or list
        -e                      webmaster email
        -w                      domain name (eg example.com)
        -n                      name of the virtual host (if not specified it uses
                                DOMAIN_NAME)
        -d                      directory name of the root directory (if not specified it uses
                                VHOST_NAME)
        -u                      username
        -m                      NOT_MAKE_DIR
        -v                      verbose
        -h                      this help	
```
## How to install

Simply clone this repo

```bash
git clone https://github.com/unnikked/Apache-VirtualHost-Manager.git
```

and then add execution permission to the script

```bash
chmod +x Apache-VirtualHost-Manager/vhost-manager.sh
```

## Example
```bash
./vhost-manager.sh -a create -e webmaster@example.com -w example.com -n example -u example [-m ignore]
```

I suggest you to add this script either on your bash path envirornment or on your `/usr/bin` folder

# JTSDK-Tools and .Net Core Applications
This repository is designed to work specifically with the JTSDK Version 3 series
tool-chain. It would be of little use elsewhere.

Delivery will be a continious release integration of the `master` branch. Unless
otherwise noted, there will be no `branches` or `tags` tracked on the server. If
circumstances mandate a change in this approach, `tags` will be placed in the
[release section](https://github.com/KI7MT/jtsdk-dotnet-core/releases).

## Supported Operating Systems
At present, this repository only supports Windows. Later releases with include
generic Linux support, and additional Ubuntu / Debian specific artifacts.

### Windows
* Win-10 x86-64 / x86-32
* Win-7|8 x86-64 / x86-32, in theory, but not tested.
* Win-XP and Vista are not supported.

### Linux
* Linux - Unsupported at this time.
* Arm Devices - Unsupported at this time.

>Note - The Core tool-chain does not require x86-64 bit applications. However,
it is highly recommended to use x86-64 if your hardware supports it.

## Supported Tool Chain
* [JTSDK-Tools v3.0.0-7 Beta](https://sourceforge.net/projects/jtsdk/files/win32/3.0.0/beta-testing/)

As the tool-chain is updated, this package will track with those changes.

## Prerequisites
In order to checkoiut and build this package, the user must have have two
utilities installed at the `system level`:
* [Git for Windows](https://git-scm.com/) (or comprable Git Client)
* Microsoft [.Net Core SDK v2.1.300](https://www.microsoft.com/net/download/windows)
or later

Both packages must be available from a standard Windows Console. If not, users
should add--either locally or system wide--the path locations to allow access to
both `git` and `dotnet` command line tools. Using the commands `git --version`
and `dotnet --info` should render without error.

## Installation
Installation of this package should follow the tool-chain installation and
setup.

```
# Open a Windows Console, then change directories to the JTSDK-Tools installation
cd /d (C|D):\JTSDK-Tools

# Set Temporary JTSDK_HOME variable
set JTSDK_HOME=%CD%

# Make a Source Directory
mkdir src

# Change Directories and Clone
cd src
git clone https://github.com/KI7MT/jtsdk-dotnet-core.git

# Change Directories and Make Install
cd jtsdk-dotnet-core
make install
```

## Upgrade
If the source clone is still present on the system, upgrading is the same as
installation, with an additional pull command. If not, use the installation steps
from above.
```
# Change Directories To The Cloned Repository
cd /d (C|D):\JTSDK-Tools\src\jtsdk-dotnet-core

# Update Source
git pull origin master

# Install New Update
make install
```

## Bug Reports
For filing bugs and feature requests, use the [Issue Tracker](https://github.com/KI7MT/jtsdk-dotnet-core/issues)


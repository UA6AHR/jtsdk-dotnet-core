# JTSDK Net Core Applications
This repository is designed to work specifically with the JTSDK Version 3 series
tool-chain. It would be of little use elsewhere.

Delivery will be directly from the `master` branch. `Branches` will be used for
development and testing, while reserving the `master` branch in a stable
condition for end users. `Tags` will be use to archive milestones and will appear
in the [release section](https://github.com/KI7MT/jtsdk-dotnet-core/releases).

## Bug Reports and Feature Requests
For submitting bug reports and feature requests, use the [Issue Tracker](https://github.com/KI7MT/jtsdk-dotnet-core/issues).

One of the main faulre points of `JTSDK v2` was the lack of flexablity and absence
of user request tracking. The aim of `JTSDK-Tools` is to use an Agile delivery
approach to create a high-quality, yet flexable build system. Utilizing Githubs 
[Issue Tracker](https://github.com/KI7MT/jtsdk-dotnet-core/issues)
users can quickly see the status of any particular request, discuss the merits,
and see the final disposition.

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

>Note - The Core Tool Chain does not require x86-64 bit applications. However,
it is highly recommended to use x86-64 if your hardware supports it.

## Installation
Installation of this package should follow the tool-chain installation and
setup. If you've not already done so, review the following guides **before**
checking out and compiling the source code.

* [Tool Chain Overview](src/JTSDK.Docs/tool-chain-setup/win32/README.md)
* [Prerequisite Tools Install](src/JTSDK.Docs/tool-chain-setup/win32/jtsdk-prereq-install.md)
* [Core Tools Install](src/JTSDK.Docs/tool-chain-setup/win32/jtsdk-core-install.md)

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
# Change directories to the JTSDK-Tools installation
cd /d (C|D):\JTSDK-Tools

# Set Temporary JTSDK_HOME variable
set JTSDK_HOME=%CD%

# Change Directories To The Cloned Repository
cd /d %JTSDK_HOME%\src\jtsdk-dotnet-core

# Update Source
git pull origin master

# Install New Update
make install
```
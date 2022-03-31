# Scoop Quick Start Guide

Scoop makes installing apps on Windows as easy as homebrew or apt.

## Requirements

Windows 10 has everything installed that you need to get started. If you are running an older version of Windows, [check the requirements](https://github.com/lukesampson/scoop#requirements).

PowerShell needs permission to execute scripts. To grant it that permission, run the command below in PowerShell.

```
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser    
```

## Installation

To install scoop, use this command.

```
iwr -useb get.scoop.sh | iex    
```

Scoop is installed in your User folder by default. To install elsewhere, refer to the [official installation instructions](https://github.com/ScoopInstaller/Scoop/wiki/Quick-Start#installing-scoop-to-custom-directory).

## Usage

To find an application, use the search command.

```
scoop search wget  
```

Install an application with the install command.

```
scoop install git  
```

Scoop collects different types of applications together in buckets. The default bucket is limited to non-GUI developer tools. To expand the number of applications available, consider adding the extras bucket.

```
scoop bucket add extras  
```

## Learn More

To see more of what scoop can do, run the help command.

```
scoop help  
```

For more extensive help, see the [Wiki](https://github.com/lukesampson/scoop/wiki).
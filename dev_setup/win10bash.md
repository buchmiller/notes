# Bash on Ubuntu on Windows

## Getting bash

This is available in Windows 10 as of the Anniversary Update.

> Press `WinKey+R`, type `winver` and press ENTER  
If the version number reads `1607`, then you have the Anniversary Update installed. The bash subsystem will use `Ubuntu 14.04`  
If the version number reads `1703`, then you have the Creators Update installed. The bash subsystem will use `Ubuntu 16.04`

To enable bash:

1. Turn on Developer mode in Settings > Update & security > For developers
1. Open Control Panel > Programs > Turn Windows features on or off
1. Enable Windows Subsystem for Linux (Beta)
1. Open the command prompt and type `bash` to install the linux subsystem

## Using bash

> [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)
> 1. DO store files in your Windows filesystem that you want to create/modify using Windows tools AND Linux tools
> 1. DO NOT create / modify Linux files from Windows apps, tools, scripts or consoles

## Java setup

Do not use the default-jre and default-jdk packages, as those use the OpenJDK/JRE vendor. We want to use the Oracle vendor.

See [http://www.wikihow.com/Install-Oracle-Java-JDK-on-Ubuntu-Linux](http://www.wikihow.com/Install-Oracle-Java-JDK-on-Ubuntu-Linux)

Or [https://stackoverflow.com/questions/36478741/installing-oracle-jdk-on-windows-subsystem-for-linux](https://stackoverflow.com/questions/36478741/installing-oracle-jdk-on-windows-subsystem-for-linux)

## Fix path

By default, the linux $PATH will include everything in the windows path. Add this to the .bashrc file to remove specific paths from $PATH.

```bash
### remove unnecessary Win PATHs
# This can prevent extension-less commands from bleeding into BASH.
# (eg. "ng" would execute the Win bin if "@angular/cli" wasn't installed on Linux.)
#
function path_remove {
  # Delete path by parts so we can never accidentally remove sub paths
  PATH=${PATH//":$1:"/":"} # delete any instances in the middle
  PATH=${PATH/#"$1:"/} # delete any instance at the beginning
  PATH=${PATH/%":$1"/} # delete any instance at the end
}
 
#path_remove '/mnt/c/Users/me/AppData/Roaming/npm'
#path_remove '/mnt/c/Program Files/Git'
#path_remove '/mnt/c/Program Files/Git/cmd'
path_remove '/mnt/c/Program Files (x86)/nodejs'
#path_remove '/mnt/c/OpenSSL-Win32/bin'
path_remove '/mnt/c/Python27'
path_remove '/mnt/c/Python27/Scripts'
path_remove '/mnt/c/Program Files/MongoDB/Server/3.2/bin'
path_remove '/mnt/c/Program Files/Apache Software Foundation/apache-maven-3.3.3/bin'
```

[Source](https://github.com/Microsoft/BashOnWindows/issues/1890#issuecomment-318802876)

To see which paths actually need to be removed:

1. Comment out all the calls to `path_remove`
1. Execute `. .bashrc` to apply any changes to `.bashrc`
1. Execute `echo $PATH` to see the current state of the linux path
1. Update the calls to `path_remove` to specify paths to be removed (each one must be specified - children of that path are not included)

## Add aliases

Create a file called .bash_aliases in the same folder as .bashrc

Add all aliases to this file, like so:

```bash
alias winhome='cd /mnt/c/Users/me'
alias dev='cd /mnt/c/dev'
```

Consider adding programs to the Windows path (which should automatically be included in the linux path too) before creating an alias for a program.

## Node

Follow the installation steps for nvm ([install steps](https://github.com/creationix/nvm#install-script))

Close the bash terminal and open it again. Type `command -v nvm` and it should print `nvm` ([verify installation](https://github.com/creationix/nvm#verify-installation))

Use nvm to install node ([nvm usage](https://github.com/creationix/nvm#usage))

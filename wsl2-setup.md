
# WSL Instalation!

## 1 - Enable the Windows Subsystem for Linux
```PowerShell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

## 2 - Enable Virtual Machine feature
```PowerShell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

## 3 - Download the Linux kernel update package
[Microsoft Official WSL2 Linux kernel update package for x64 machines](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

## 4 - Set WSL 2 as your default version
```PowerShell
wsl --set-default-version 2
```

## 5 - Install Linux distribution
 - [Debian](https://www.microsoft.com/en-us/p/debian/9msvkqc78pk6)
 - [Ubuntu](https://www.microsoft.com/en-us/p/ubuntu/9nblggh4msv6)


## 6 - Set Linux distribution version to WSL 1 or WSL 2
```PowerShell
wsl --set-version <distribution name> <versionNumber>
```
#### Example:
```PowerShell
wsl --set-version Debian 2
```

#### Version 2 by default (recommended):
```PowerShell
wsl --set-default-version 2
```

## 7 - Configure WSL2 Settings
##### Create a new file identified by '.wslconfig' in the user's root folder, include the necessary settings for it to work on your computer.
```Text
[wsl2]

memory=2GB # How much memory to assign to the WSL2 VM.

processors=5 # How many processors to assign to the WSL2 VM.

kernel= # An absolute Windows path to a custom Linux kernel.

swap= # How much swap space to add to the WSL2 VM. 0 for no swap file.

swapFile= # An absolute Windows path to the swap vhd.

localhostForwarding= # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).
```

### References
 - [Microsoft Official Article](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
 - [OMG! Ubuntu!](https://www.omgubuntu.co.uk/how-to-install-wsl2-on-windows-10)

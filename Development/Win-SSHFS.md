# Win-SSHFS 

#### Relevant links
[Dokan](https://github.com/dokan-dev/dokany/releases) (Confirmed working with [Dokan 1.0.1.1000](https://github.com/dokan-dev/dokany/releases/tag/v1.0.1) )

[Win-SSHFS Foreveryone](https://github.com/feo-cz/win-sshfs/releases) 


### What is it?

A tool that mounts an ssh filesystem to the Windows filesystem, allowing remote files to be used as if they were local

### Installation

 * Install [Dokan](https://github.com/dokan-dev/dokany/releases). (Either run the setup.exe, or the msi installer)
 * Install [Win-SSHFS Foreveryone](https://github.com/feo-cz/win-sshfs/releases) by running the .msi file
 * Configure a new drive by specifying Drive Name, Host, Username, and Authentication method. 
 * Save contiguration and mount drive



### Limitations

This tool doesn't actively synchronize changes from the remote file system. For example if files in a remote directory are listed in the file explorer, any changes to that directory not done by the current user will not be seen until the list of files is reloaded.




**Update Aug 2019**: Experiencing Blue Screens of Death caused by Page Faults due to Dokan 1.0.1 . Newer versions of Dokan do not seem to work with Win-Sshfs.

Luckily, Windows Subsystem Linux 2 (WSL2) was just released to Windows Insider Fast Ring. This provides a full Linux Kernel with interoperability with the Windows FileSystem.

Current solution is to enable WSL2, mount ssh filesystem using [sshfs](https://github.com/libfuse/sshfs), and access mounted drive from the Windows FS 

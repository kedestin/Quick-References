# WSL2 + sshfs

#### Relevant links
[WSL2](https://docs.microsoft.com/en-us/windows/wsl/wsl2-install) - Improvement to the original Windows Subsystem Linux, that brings compatability with many network related Linux programs (i.e fuse and sshfs)

[sshfs](https://github.com/libfuse/sshfs) - Mounts remote filesystems to a local directory


### What is it?

A combination of Windows' built in linux environment and a Linux filemounting utility that together  mount a remote filesystem to the Windows filesystem, allowing remote files to be used as if they were local.

### Getting Started

 * Enable [WSL2](https://docs.microsoft.com/en-us/windows/wsl/wsl2-install). *Note:* Until WSL2 is available in the mainstream version of windows, this may require that you join the Windows Insider program.
 * Install [sshfs](https://github.com/libfuse/sshfs) if not already installed.
`sudo apt-get install -y sshfs`


### To use

From sshfs' documentation

>Once sshfs is installed (see next section) running it is very >simple::

    sshfs [user@]hostname:[directory] mountpoint


>To unmount the filesystem::

    fusermount -u mountpoint

>On BSD and macOS, to unmount the filesystem::

    umount mountpoint
# Pakcage management

## RPM and YUM

## DPKG and APT

### DPKG

Debian package manager, low-level package manager.
isntall, remove, upgrade, list and verify packages.

`dkpg -i` to install
`dkpg -r` to uninstall
`dkpg -l` to list
`dkpg -s` to check the status of the packafge  
`dkpg -r` to verify pcakge

Smilar to RPM, does not honor the depenency

#### APT/APT-GET

APT: advanced package manager. More user frendly and easier on the eye thatn APT-GET.

`/etc/apt/sources.list`

`apt update` to refresh the repository. downlaod package information.
`apt upgrade` to unstall all upgrade from the system
`apt edit-sources` to change the source repositories in `/etc/apt/source.list`
`apt install` to isntall a package
`apt remove` to remove a package
`apt search` search in the repositloy
`apt list | grep`

# Ansible Role Raspberry Pi Imager
This is an Ansible role that installs Raspberry Pi Imager on Linux. It compiles it from source on RHEL there is no official package for RHEL-based distros..  

The package is only available for x86_64, you can manually set `rpi_imager_compile` to compile it on Debian instead of using the package.  

# WARNING
Since this will be compiled from source on RHEL, it will need to download a LOT of dependencies. This will take a while. It will also take a while to compile.  

Tested on Fedora 36 and Ubuntu 22.04, should work on any Linux distribution supported by the Debian package or one that has the necessary build dependencies.

## Requirements

### Base requirements
None  

## Variables
| Variable | Default | Description |
|----------|---------|-------------|
| `rpi_imager_version` | `1.7.3` | The version of Raspberry Pi Imager to install or compile. |
| `rpi_imager_compile` | `true` on Debian-based distros, `false` on RHEL-based distros | Whether to compile Raspberry Pi Imager from source. |
| `rpi_imager_build_deps` | See [defaults/main.yml](./defaults/main.yml) | Dict of list of build dependencies |
| `rpi_imager_deb_url` | See [defaults/main.yml](./defaults/main.yml) | URL to download the Debian package from. |

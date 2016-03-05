![Hoa](http://static.hoa-project.net/Image/Hoa_small.png)

Hoa is a **modular**, **extensible** and **structured** set of PHP libraries.
Moreover, Hoa aims at being a bridge between industrial and research worlds.

# Provisioners

This directory contains provisioners for different machines. There is one
provisioner per service. Each provisioner contains scripts and resources grouped
by machine type.

The special `_Prelude` provider contains preludes grouped by machine type. A
prelude prepares the environment for all scripts, ensuring a consistent script
behavior everywhere. In addition, it provides useful common functions and
install common tools.

## Organisation

We find the following directories:

  * `Nginx`, contains nginx provisioner,
  * `_Prelude`, contains preludes.

All provisioners exposes the following Provisioner Interface (Π):

  * `Requirements`, to check whether the provisioned service can be
    installed,
  * `Install`, to install and to configure the service,
  * `Test`, to test the service (after the installation succeed or at any
    time),
  * `Backup`, to save or to restore data of the service.

Ensure the appropriated prelude has been sourced before using the Π.

## Tools

Scripts are written in [Bash](https://www.gnu.org/software/bash/). They follow
[the Shell Style Guide](https://google.github.io/styleguide/shell.xml).

Tests are written using [`bats`](https://github.com/sstephenson/bats).

## Documentation

Different documentations can be found on the website:
[http://hoa-project.net/](http://hoa-project.net/).

## License

Hoa is under the New BSD License (BSD-3-Clause). Please, see
[`LICENSE`](http://hoa-project.net/LICENSE).

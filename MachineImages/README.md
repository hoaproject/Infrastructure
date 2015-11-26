![Hoa](http://static.hoa-project.net/Image/Hoa_small.png)

Hoa is a **modular**, **extensible** and **structured** set of PHP libraries.
Moreover, Hoa aims at being a bridge between industrial and research worlds.

# Machine images

This directory contains the tools and configurations to create all kind of
machine images we are likely to use in our infrastructure (which includes the
continuous integration service, so potentially a lot of different machines).

## Organisation

We find the following directories:

  * `Artifacts`, contains all the resulting machine images,
  * `Templates`, contains all the template/configuration files to create
    artifacts.

## Tools

We use [Packer](https://packer.io/) to build all our machine images. See [the
requirements to install it](https://packer.io/downloads.html).

To pre-provisionning the machine images we use Shell scripts so far.

## Documentation

Different documentations can be found on the website:
[http://hoa-project.net/](http://hoa-project.net/).

## License

Hoa is under the New BSD License (BSD-3-Clause). Please, see
[`LICENSE`](http://hoa-project.net/LICENSE).

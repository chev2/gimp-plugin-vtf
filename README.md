gimp-plugin-vtf
===============

A plugin to open and save VTF files in GIMP on Linux.

Originally developed by [lxndr](https://github.com/lxndr), with additional fixes & changes to ensure compatibility on Linux.

## Installation

### Arch Linux

There is a PKGBUILD included with the repository.

Clone the git repositroy:

```console
git clone https://github.com/linux-source-tools/gimp-plugin-vtf.git
```

Then, run `makepkg`:

```console
makepkg -s PKGBUILD
```

### Debian / Ubuntu

Clone the git repository into a folder you want to save it to:

```console
git clone https://github.com/linux-source-tools/gimp-plugin-vtf.git
```

Install the required libraries:

- `libgimp2.0-dev`

- `liblcms2-dev`

- `libsquish-dev`

- `libsquish0`

You can install all of these with:

```bash
sudo apt install libgimp2.0-dev liblcms2-dev libsquish-dev libsquish0 libboost1.74-dev  libboost-iostreams-dev     
```

`cd` into the new directory, then make `file-vtf` with:

```console 
make
```

After compiling, move `file-vtf` to your GIMP plugins folder, such as `/usr/lib/gimp/2.0/plug-ins/`.

The final path should be `/usr/lib/gimp/2.0/plug-ins/file-vtf`.

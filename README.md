# CleanRSD [![License](http://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

**CleanRSD** setups removable storage devices (RSDs) such as USB flash drives, SD cards and removable hard drives, so that they aren't polluted by self-serving, shameful, indelicate programs. This saves some space, and more importantly speeds up the device and extends its lifetime.

## Features

CleanRSD currently does the following:
* Create two files named `IF YOU FIND THIS.TXT` and `SI VOUS TROUVEZ CECI.TXT` at the root directory of the device, respectively in English and in French. That may help if you ever lose your device — through it doesn't replace proper backups.
* Prevent Apple file system events daemon from writing filesystem logs to the `.fseventsd` directory.
* Prevent Apple Spotlight from snooping into your data and writing its search index to the `.Spotlight-V100` directory.
* Prevent Apple Mac OS X from writing deleted files to the `.Trashes` and `._.Trashes` directories.
* Clean up `.DS_Store` directories left by Apple Finder as well as `Thumbs.db` and `desktop.ini` files and the `System Volume Information` and `$RECYCLE.BIN` directories left by Microsoft Windows Explorer.

## Installation

Just copy the `cleanrsd` file where you want, edit it to customize the `IF YOU FIND THIS.TXT` and `SI VOUS TROUVEZ CECI.TXT` files, and make it executable (`chmod a+x cleanrsd`).

## Usage

Run `cleanrsd <path to the removable storage device mount point>`

## Recommendations

CleanRSD improves a bit over doing nothing with your removable devices. However, you should keep in mind that the right answers to these issues are:
* Never lend a removable device to anyone running an Apple or Microsoft operating system, as these are shameless, untrustworthy pieces of crap.
* More generally, never lend a removable device to anyone you don't trust to be 1) trustworthy and 2) competent enough to avoid crappy software.
* If you ever *have* to lend a removable device, make sure that it's readonly (*hardware* readonly). Not only will it prevent the inconveniences CleanRSD fights against more reliably than it does, but it will also protect you from data tempering and malware. If you don't trust whoever you lend the device, though, it's still no guarantee.
* Never accept a removable device from anyone you wouldn't lend one to. Not only could it contain malware (including firmware exploits), but it could also be a fake storage device and a real input device (yes, such things exist), or a so-called USB-killer device, which can physically destroy your computer or part thereof.
* Always have proper backups of what is on your removable storage devices. You can't avoid losing them or having them stolen, and these have a rather short lifetime anyway.
* Always use proper encryption for sensitive data on your removable storage devices. You can't avoid losing them or having them stolen or copied.

## Roadmap

CleanRSD would like to add the following features:
* Prevent Microsoft Windows Explorer from writing image thumbnails to the `Thumbs.db` file.
* Prevent Microsoft Windows Explorer from writing display settings to the `desktop.ini` file.
* Prevent Microsoft Windows Explorer from writing device information to the `System Volume Information` directory.
* Prevent Microsoft Windows Explorer from writing deleted files  to the `$RECYCLE.BIN` directory.
* Prevent Apple Finder from writing information to the `.DS_Store` directory.

If you know how to implement this features, please let me know!

## Contributing and reporting bugs

Contributions are welcome through [GitHub pull requests](https://github.com/Arkanosis/CleanRSD/pulls).

Please report bugs and feature requests on [GitHub issues](https://github.com/Arkanosis/CleanRSD/issues).

## License

CleanRSD is copyright (C) 2017 Jérémie Roquet <jroquet@arkanosis.net> and licensed under the MIT license.

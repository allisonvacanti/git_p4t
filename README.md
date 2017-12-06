<!--
Distributed under the MIT License
http://www.opensource.org/licenses/mit-license.php
-->

This repository contains a modified version of `git-p4.py` (which is part of
the main [Git] distribution) with some extra functionality required by
[NVIDIA's CUDA Thrust library]. It has the following added features:

* Automatic insertion of Git commit hashes and Git author ids into Perforce changelist descriptions.

Parts of the code are distributed under the [GNU Public License version 2
(GPLv2)] and parts of the code are distributed under the [MIT License]. See
[LICENSE.md](LICENSE.md) for further details.

Dependencies
============

**Required Dependencies**

| [Python]                            | 2.7.13 |
| [GNU Bash]                          | 4.2    |
| [GNU Make]                          | 4.1    |
| [Git]                               | 2.6.4  |
| [Perforce Command-Line Client (p4)] | 2017.1 |

**Optional Dependencies**

These are needed to build the git-p4 manpage.

| [AsciiDoc]                          | 8.6.9 |
| [DocBook]                           | 4.5   |
| [xmlto]                             | 0.0.2 |

Note that to install the Perforce Command-Line Client (p4) on Debian or Ubuntu
systems, you'll first need to add their Debian package repository to your list
of Debian package sources:

```
deb http://package.perforce.com/apt/ubuntu trusty release
```

The following commands will add it and update the list of available packages:

```bash
sudo bash -c 'echo "deb http://package.perforce.com/apt/ubuntu trusty release" > /etc/apt/sources.list.d/perforce.list'
sudo apt-get update
```

After you've done that, the following will install all dependencies on Debian
or Ubuntu systems:

```bash
sudo apt-get install python bash make git perforce-cli asciidoc docbook xmlto
```

[NVIDIA's CUDA Thrust library]:                 https://thrust.github.com
[GNU General Public License version 2 (GPLv2)]: https://opensource.org/licenses/GPL-2.0
[MIT License]:                                  https://opensource.org/licenses/mit-license.php
[Python]:                                       https://python.org
[GNU Bash]:                                     https://www.gnu.org/software/bash
[GNU Make]:                                     https://www.gnu.org/software/make
[Git]:                                          https://git-scm.com
[Perforce Helix Command-Line Client (p4)]:      https://www.perforce.com/downloads/helix-command-line-client-p4
[AsciiDoc]:                                     https://asciidoc.org
[DocBook]:                                      https://docbook.org
[xmlto]:                                   https://pagure.io/xmlto

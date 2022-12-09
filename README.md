=================================================================================================================================================
Own build info


mkdir buildQuaZip
cd buildQuaZip

cmake .\.. -G "Visual Studio 17 2022" -A x64 -DCMAKE_INSTALL_PREFIX=.\..\install2\ -D QUAZIP_QT_MAJOR_VERSION=5 -Wno-dev -D QUAZIP_USE_QT_ZLIB=ON -DCMAKE_BUILD_TYPE=RelWithDebInfo
cmake --build . --target ALL_BUILD --config RelWithDebInfo
cmake -DBUILD_TYPE=RelWithDebInfo -P cmake_install.cmake

=================================================================================================================================================

QuaZip is the C++ wrapper for Gilles Vollant's ZIP/UNZIP package
(AKA Minizip) using Trolltech's Qt library.

If you need to write files to a ZIP archive or read files from one
using QIODevice API, QuaZip is exactly the kind of tool you need.

See [the documentation](https://stachenov.github.io/quazip/) for details.

Want to report a bug or ask for a feature? Open an [issue](https://github.com/stachenov/quazip/issues).

Want to fix a bug or implement a new feature? See [CONTRIBUTING.md](CONTRIBUTING.md).

You're a package maintainer and want to update to QuaZip 1.0? Read [the migration guide](https://github.com/stachenov/quazip/blob/master/QuaZip-1.x-migration.md).

Copyright notice:

Copyright (C) 2005-2020 Sergey A. Tachenov and contributors

Distributed under LGPL, full details in the COPYING file.

Original ZIP package is copyrighted by Gilles Vollant, see
quazip/(un)zip.h files for details, but basically it's the zlib license.

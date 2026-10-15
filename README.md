# SQLITE

> SQLite Source Repository This repository contains the complete source code for the [SQLite database engine](https://sqlite.org/) going back to 2000-05-29. The tree includes many tests and some documentation, though additional tests and most documentation are managed separately.

**Category:** MOBILE · **Ecosystem:** unknown · **Vendored upstream:** https://github.com/sqlite/sqlite · **Pinned commit:** `90687aa700d1d0a7af8fe95f8a4c841df6fa15ba` · **Vendor:** Anticloud FZ LLE

## What This Project Is

SQLite Source Repository This repository contains the complete source code for the [SQLite database engine](https://sqlite.org/) going back to 2000-05-29. The tree includes many tests and some documentation, though additional tests and most documentation are managed separately.

This is the upstream project, vendored at the pinned commit above and packaged offline-first. The 12 improvements Anticloud adds live in `anticloud/` and are described under *Anticloud Overlay* below. Every fact in this file traces to a file in this directory.

## Installation

```
# See the upstream README (linked above) for build steps.
```

## Usage

On Windows, everything can be compiled with MSVC.
You will also need a working installation of TCL if you want to run tests,
though TCL is not required if you just want to build SQLite itself.
See the [compile-for-windows.md](doc/compile-for-windows.md) document for
additional information about how to install MSVC and TCL and configure your
build environment.

If you want to run tests, you need to let SQLite know the location of your
TCL library, using a command like this:

        set TCLDIR=c:\Tcl

SQLite itself does not contain any TCL code, but it does use TCL to run
tests. You may need to install TCL development libraries in order to
successfully complete some makefile targets. It is helpful, but is not
required, to install the SQLite TCL extension (the "tclextension-install"
target) prior to running tests.

The source tree contains a "make.bat" file that allows the same "make"
commands of Unix to work on Windows.  In the following, you can substitute
"nmake /f Makefile.msc" in place of "make", if you prefer to avoid this BAT
file:

        make sqlite3.exe
        make sqlite3.c
        make sqldiff.exe

## Anticloud Overlay

The 12 improvements live under `anticloud/`. Run the check suite from this directory:

```
python anticloud/bench/runner.py --cwd anticloud
```

## Benchmark Results

The suite is recorded in `BENCH.json`; no benchmark rows were found in this package.

## Licence

The upstream licence is preserved in `LICENSE` and `THIRD_PARTY_LICENSES/`. The Anticloud overlay is licensed under Anticommons 0.1.0 (`ANTICOMMONS_LICENSE.md`).

## Verification

SHA3-256 of `BENCH.json`:

```
97e0d9b65f36b267fe39ebbc194175cf95228088d04187f20a5b674e583d1ba8
```

Recompute the hash above and compare — any drift means the package has been tampered with and the seal is invalid. This is a self-assessment; no external audit has been performed and a SOC 2 / NIST independent audit is committed post-funding.

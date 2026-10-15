# SQLITE

> Anticloud offline package — upstream: sqlite/sqlite @ `master`.

## What This Project Does

Official Git mirror of the SQLite source tree

## Upstream README

<h1 align="center">SQLite Source Repository</h1>

This repository contains the complete source code for the
[SQLite database engine](https://sqlite.org/) going back
to 2000-05-29.  The tree includes many tests and some
documentation, though additional tests and most documentation
are managed separately.

See the [on-line documentation](https://sqlite.org/) for more information
about what SQLite is and how it works from a user's perspective.  This
README file is about the source code that goes into building SQLite,
not about how SQLite is used.

## Version Control

SQLite sources are managed using
[Fossil](https://fossil-scm.org/), a distributed version control system
that was specifically designed and written to support SQLite development.
The [Fossil repository](https://sqlite.org/src/timeline) contains the urtext.

If you are reading this on GitHub or some other Git repository or service,
then you are looking at a mirror.  The names of check-ins and
other artifacts in a Git mirror are different from the official
names for those objects.  The official names for check-ins are
found in a footer on the check-in comment for authorized mirrors.
The official check-in name can also be seen in the `manifest.uuid` file
in the root of the tree.  Always use the official name, not  the
Git-name, when communicating about an SQLite check-in.

If you pulled your SQLite source code from a secondary source and want to
verify its integrity, there are hints on how to do that in the
[Verifying Code Authenticity](#vauth) section below.

## Contacting The SQLite Developers

The preferred way to ask questions or make comments about SQLite is to
visit the [SQLite Forum](https://sqlite.org/forum) at
<https://sqlite.org/forum/>.  Anonymous postings are permitted. For
bug reports, please use the [SQLite bugs
forum](https://sqlite.org/bugs) at <https://sqlite.org/bugs>.

If you think you have found a bug that has security implications and
you do not want to report it on the public forum, you can send a private
email to drh at sqlite dot org.

## Public Domain

The SQLite source code is in the public domain.  See
<https://sqlite.org/copyright.html> for details. 

Because SQLite is in the public domain, we do not normally accept pull
requests, because if we did take a pull request, the changes in that
pull request might carry a copyright and the SQLite source code would
then no longer be fully in the public domain.

## Obtaining The SQLite Source Code

Source code tarballs or ZIP archives are available at:

  *  [Latest trunk check-in](https://sqlite.org/src/rchvdwnld/trunk).

  *  [Latest release](https://sqlite.org/src/rchvdwnld/release)

  *  For other check-ins, browse the
     [project timeline](https://sqlite.org/src/timeline?y=ci) and
     click on the check-in hash of the check-in you want to download.
     On the resulting "info" page, click one of the options to the
     right of the "**Downloads:**" label in the "**Overview**" section
     near the top.

To access

## License

Upstream terms preserved in `THIRD_PARTY_LICENSES/`. Overlay licensed under Anticommons 0.1.0.

## Verification

Recompute the SHA3-256 of `BENCH.json` and compare to this package’s register. Any drift = invalid package.

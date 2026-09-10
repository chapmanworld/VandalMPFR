# VandalMPFR

**VandalMPFR** is a pinned fork of the [GNU MPFR](https://www.mpfr.org/) arbitrary-precision floating-point library, used as a build-time dependency of GDB in the **VandalSDK** toolchain (see `VandalBinUtils`).

This is **not Vandal-authored code**. It is a fork of an existing, independently maintained open-source project, imported here purely so that a specific, known-good version can be built reproducibly as part of the VandalSDK toolchain used by the **Vandalism Engine** game engine.

## Baseline

See `VANDALMPFR_BASELINE.txt` for the exact upstream version, tag, and repository this fork was taken from.

## Why this repository exists

VandalSDK's packaged debugger (GDB) links against MPFR for arbitrary-precision arithmetic support. Pinning a specific MPFR release as its own repository, alongside the other GDB build dependencies (`VandalGMP`, `VandalMPC`, `VandalISL`), gives the SDK toolchain build a reproducible, independently versioned source for each dependency, separate from upstream's own release cadence.

This repository exists for internal use while building Vandalism Engine and its SDK. It is not a general-purpose MPFR distribution.

## Contributions and issue tracking

This is **not a maintained fork**. Craig Chapman is not accepting contributions here, and this repository is not the place to raise issues, ask questions, or request features.

* Please do not use this repository as an MPFR support forum.
* Please do not raise issues here for upstream MPFR bugs.
* Please do not use this repository to report Vandal Engine or VandalSDK bugs.
* Issues with MPFR itself should be raised with the upstream MPFR project.

## Licensing

MPFR is distributed under the **GNU Lesser General Public License (LGPL) version 3 or later**. See `COPYING` and `COPYING.LESSER` in this repository for the authoritative upstream license terms.

## Status

Toolchain dependency fork. Tracks a single pinned upstream release for VandalSDK build reproducibility.

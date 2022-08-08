# asdf-polaris

[![Build Status](https://travis-ci.org/TheCubicleJockey/asdf-polaris.svg?branch=master)](https://travis-ci.org/TheCubicleJockey/asdf-polaris)

polaris plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

## Install

```
asdf plugin-add polaris https://github.com/TheCubicleJockey/asdf-polaris.git
```

## Use

Check out the [asdf documentation](https://asdf-vm.com/#/core-manage-versions?id=install-version) for instructions on how to install and manage versions of polaris.

## Architecture Override
The `ASDF_polaris_OVERWRITE_ARCH` variable can be used to override the architecture that is used for determining which `polaris` build to download. The primary use case is when attempting to install an older version of `polaris` for use on an Apple M1 computer as `polaris` was not built for ARM at the time.

### Without `ASDF_polaris_OVERWRITE_ARCH`:

```
% asdf install polaris 1.24.3
Downloading polaris from https://storage.googleapis.com/kubernetes-release/release/v1.18.17/bin/darwin/arm64/polaris
```

### With `ASDF_polaris_OVERWRITE_ARCH`:

```
% ASDF_polaris_OVERWRITE_ARCH=amd64 asdf install polaris 1.18.17
Downloading polaris from https://storage.googleapis.com/kubernetes-release/release/v1.18.17/bin/darwin/amd64/polaris
```


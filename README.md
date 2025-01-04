# vproweather

A *nix tool for querying the _original_ Davis Vantage Pro.

This is a fork of `vproweather-0.6` from Joe Jaworski. You can find the original
code at the tag `v0.6` or from the [horse's
mouth](http://www.joejaworski.com/weather/).

## Building

This code is built with Bazel. This allows the whole build to be fully
specified, not dependent on whatever compiler you have installed (or installing
a compiler at all). You don't even have to install Bazel! You just need `bazelisk`.

### Get Bazelisk

This is a single-file static binary that wraps Bazel itself, fetching and
executing the version of Bazel defined in the repo. Download the latest release
of `bazelisk` [from here](https://github.com/bazelbuild/bazelisk). It is
recommended that you name this binary `bazel` and place it in your path (perhaps
`/usr/local/bin`), so you can use it as a stand-in for the original article.

### Execute the build

```shell
bazel build :vproweather
```

### Install the binary

The executable will be in `bazel-bin/vproweather`. It is fully static, so it
will run on any system of the same architecture. Just copy the file to where you
want it to be.

## Running

Just run the binary for usage info.

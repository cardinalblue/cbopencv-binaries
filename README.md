# cbopencv-binaries

This repository hosts precompiled binary artifacts (such as `.xcframework.zip` files) used by the [cbopencv-spm](https://github.com/cardinalblue/cbopencv-binaries/) Swift Package.

## Purpose

Swift Package Manager requires binary targets to be publicly accessible via a direct URL. Since GitHub private repositories do not allow unauthenticated binary downloads, this repository provides a public release point for hosting OpenCV-related binary frameworks used across Cardinal Blue projects.

## Contents

- ✅ Precompiled `.xcframework.zip` files for use with `binaryTarget(url:)` in Swift packages
- ✅ Versioned releases that match corresponding tags in [`cbopencv-spm`](https://github.com/cardinalblue/cbopencv-spm)
- ✅ SHA256 checksum-friendly structure for secure SPM integration

## Usage

To use a hosted binary in your `Package.swift`:

```swift
.binaryTarget(
    name: "opencv2",
    url: "https://github.com/cardinalblue/cbopencv-binaries/releases/download/1.0.0/opencv2.xcframework.zip",
    checksum: "<insert-checksum-here>"
)
```

## Notes
- This repository contains no source code.
- Each release must include a valid .zip file containing the expected .xcframework structure.

For issues or updates, please refer to the main repository.
- https://github.com/cardinalblue/cbopencv-binaries/issues
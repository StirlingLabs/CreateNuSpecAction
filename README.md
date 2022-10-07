# 📦 Create NuSpec Action

> Create a NuSpec file according to the parameters provided

## ⭐ Features

- This just creates a .NuSpec file.

## 🚀 Quickstart

```yaml
      # Store this asset in 'gh-storage' branch.
      - name: Create NuSpec
        uses: StirlingLabs/CreateNuSpecAction@main
        with:
          id: StirlingLabs.sockaddr.Net.runtime.${{ matrix.runtime }}.libsa
          version: 22.10.0
          title: sockaddr.Net
          description: |
            sockaddr.Net provides cross-platform socket address bindings for .Net, using the libsa project.
            This package provides the libsa library on ${{ matrix.runtime }} for consumption by sockaddr.Net.
          authors: The Stirling Labs Team
          etc: ...

      # Generate an asset in your job. E.G: Download a badge image from shields.io
      - name: Create NuPkg
        run: nuget pack sockaddr.nuspec
```

## Parameters

|Name|Function|
|-|-|
|id|The NuPkg ID (e.g. StirlingLabs.Utilities.Magic)|
|version|Package version number.|
|title|Display title of the NuPkg, visible on nuget.org.|
|description|Description of the NuPkg, indexed and visible on nuget.org.|
|authors|Metadata authors of the NuPkg.|
|etc|...|
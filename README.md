# 📦 Preflight Dotnet Project Action

> Preflight a Solution and Project files according to Stirling Labs' standards

## ⭐ Features

- Ensures that the project is set up correctly to integrate with our other Actions, scripts, etc.

## 🚀 Quickstart

```yaml
      - name: Preflight
        id: preflight
        if: runner.os == 'Linux'
        uses: StirlingLabs/PreflightDotnetAction@main
        with:
          coreName: ${{ needs.meta.outputs.coreName }}
          solution: ${{ inputs.solution }}
          gitUrl: ${{ needs.meta.outputs.gitUrl }}
          homepage: ${{ needs.meta.outputs.homepage }}
          defaultBranch: ${{ needs.meta.outputs.defaultBranch }}
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
# ![StirlingLabs.Tests](https://raw.githubusercontent.com/StirlingLabs/PreflightDotnetAction/main/PreflightAction.jpg)

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
          solution: name.sln
          library: true
          strict: true
          verbose: true
```

## Parameters

|Name|Function|
|-|-|
|solution|string|Path to the .sln|optional|
|library|boolean|Does this project produce a library (as opposed to executable)?|true|
|strict|boolean|Be strict with compliance?|true|
|verbose|boolean|Verbose output or terse?|true|
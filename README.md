# Go Release Binary GitHub Action

Automate publishing Go build artifacts for GitHub releases through GitHub Actions

```yaml
# .github/workflows/release.yaml

on: release
name: Build
jobs:
  release-linux-386:
    name: release linux/386
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: compile and release
      uses: mjavier2k/go-release.action@v1.1.2
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        GOARCH: "386"
        GOOS: linux
        EXECUTABLE_NAME: "solidfire-exporter"
        EXECUTABLE_PATH: "./cmd/solidfire-exporter"
        PACKAGE: "./cmd/solidfire-exporter/main.go"
  release-linux-amd64:
    name: release linux/amd64
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: compile and release
      uses: mjavier2k/go-release.action@v1.1.2
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        GOARCH: amd64
        GOOS: linux
        EXECUTABLE_NAME: "solidfire-exporter"
        EXECUTABLE_PATH: "./cmd/solidfire-exporter"
        PACKAGE: "./cmd/solidfire-exporter/main.go"
  release-darwin-386:
    name: release darwin/386
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: compile and release
      uses: mjavier2k/go-release.action@v1.1.2
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        GOARCH: "386"
        GOOS: darwin
        EXECUTABLE_NAME: "solidfire-exporter"
        EXECUTABLE_PATH: "./cmd/solidfire-exporter"
        PACKAGE: "./cmd/solidfire-exporter/main.go"
  release-darwin-amd64:
    name: release darwin/amd64
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: compile and release
      uses: mjavier2k/go-release.action@v1.1.2
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        GOARCH: amd64
        GOOS: darwin
        EXECUTABLE_NAME: "solidfire-exporter"
        EXECUTABLE_PATH: "./cmd/solidfire-exporter"
        PACKAGE: "./cmd/solidfire-exporter/main.go"
  release-windows-386:
    name: release windows/386
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: compile and release
      uses: mjavier2k/go-release.action@v1.1.2
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        GOARCH: "386"
        GOOS: windows
        EXECUTABLE_NAME: "solidfire-exporter"
        EXECUTABLE_PATH: "./cmd/solidfire-exporter"
        PACKAGE: "./cmd/solidfire-exporter/main.go"
  release-windows-amd64:
    name: release windows/amd64
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: compile and release
      uses: mjavier2k/go-release.action@v1.1.2
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        GOARCH: amd64
        GOOS: windows
        EXECUTABLE_NAME: "solidfire-exporter"
        EXECUTABLE_PATH: "./cmd/solidfire-exporter"
        PACKAGE: "./cmd/solidfire-exporter/main.go"
```

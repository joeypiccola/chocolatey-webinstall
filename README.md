# chocolatey-webinstall

This is a modifed verson of https://chocolatey.org/install.ps1 that is setup to 1) retrieve a chocolatey nupkg package from a local repo and 2) unzip it using Expand-Archive.

### Local repo
Modify the following line so that it points to your repo.

```powershell
$env:chocolateyDownloadUrl = 'https://artifactory.-.com/artifactory/api/nuget/nuget-local/chocolatey.0.10.3.nupkg'
```

### Installing chocolatey
Open PowerShell and type the following. Nothing amazing here. 

```powershell
iwr http://something.internal/choco/install.ps1 -UseBasicParsing | iex
```
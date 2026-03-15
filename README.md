# win11-tiny

Release assets for the tiny Windows 11 VM archive, base on https://github.com/ntdevlabs/tiny11builder

## Base Image

VMware ready-to-go version:
https://archive.org/details/windows-11-tiny-vmware-image

i made a newer version of image base on above image to current repo release page :
https://github.com/q2333gh/win11-tiny

```text
upgrade its vmware verison of 12 to 17.5
disable 3d acceleration because its screen flash on my machine
disable all os animation
installed firefox using curl.
```

## Release

Current release:
https://github.com/q2333gh/win11-tiny/releases/tag/v2026-03-15

Files in this release:

```text
win11_tiny_release.7z.001
win11_tiny_release.7z.002
win11_tiny_release.7z.003
```

## PowerShell One-Liner

Copy and run this in PowerShell to download the full archive set for this release:

```powershell
$d = "$HOME\Downloads\win11-tiny-v2026-03-15"
mkdir -Force $d | Out-Null

iwr `
  https://github.com/q2333gh/win11-tiny/releases/download/v2026-03-15/win11_tiny_release.7z.001 `
  -OutFile "$d\win11_tiny_release.7z.001"

iwr `
  https://github.com/q2333gh/win11-tiny/releases/download/v2026-03-15/win11_tiny_release.7z.002 `
  -OutFile "$d\win11_tiny_release.7z.002"

iwr `
  https://github.com/q2333gh/win11-tiny/releases/download/v2026-03-15/win11_tiny_release.7z.003 `
  -OutFile "$d\win11_tiny_release.7z.003"
```

## Extract

After download, extract from `.001` with 7-Zip:

```powershell
& 'C:\Program Files\7-Zip\7z.exe' x "$HOME\Downloads\win11-tiny-v2026-03-15\win11_tiny_release.7z.001"
```

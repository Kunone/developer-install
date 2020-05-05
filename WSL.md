### install WSL2
`https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004/`
`https://www.youtube.com/watch?v=MrZolfGm8Zk`

- upgrade windows version to 2004
- search for `turn windows features on or off`
- ensure to check `virtual machine platform` and `windows subsystem for linux`
or
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

### upgrade wsl version
```
wsl -l -v
wsl --set-version ${distro} 2
wsl --set-default-version 2
```

### docker support for WSL2
- upgrade to the latest docker for windows
- open docker settings and to enable the config for `wsl2`
- choose the right `distro` for docker
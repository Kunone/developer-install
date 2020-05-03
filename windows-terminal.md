### install WSL (Windows Subsystem for Linux)
`https://docs.microsoft.com/en-us/windows/wsl/install-win10`

### install windows terminal
fix windows store:
`https://answers.microsoft.com/en-us/windows/forum/all/micxrosoft-store-error-code-0x80131500/41d2d363-83ee-4b5d-ba43-615ca63bb1bf`
###### Re-register All Store apps
```
Get-AppXPackage -AllUsers | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml"}
```
###### Uninstall & Reinstall Store
```
Get-AppxPackage -allusers *WindowsStore* | Remove-AppxPackage
Get-AppxPackage -allusers *WindowsStore* | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register “$($_.InstallLocation)\AppXManifest.xml”}
```
###### config IP
```
Search for "Internet Options"
Open the App
Select the "Advanced" Tab
Scroll to the Bottom of the List where you can see "Use SSL/TLS"
UN-Select SSL 3.0 and TLS 1.0 and 1.1
SELECT TLS 1.2
Click "Apply"
Click "OK"
Reboot Computer
```


### install brew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
### install Homebrew dependencies
```
sudo apt-get update
sudo apt-get install build-essential
```
### Configure Homebrew PATH
```
echo 'eval $(/home/linuxbrew/.linuxbrew/bin/brew shellenv)' >> /home/kun/.profile
eval $(/home/linuxbrew/.linuxbrew/bin/brew shellenv)
```

### install packages
```
brew install gcc
```

### terminal config
`https://github.com/romkatv/powerlevel10k`
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
``` OR
```
brew install romkatv/powerlevel10k/powerlevel10k
echo 'source /usr/local/opt/powerlevel10k/powerlevel10k.zsh-theme' >>! ~/.zshrc
```

### more font
`https://github.com/ryanoasis/nerd-fonts`


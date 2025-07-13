# install WSL
**Enable hyper-v**
- open `Windows cmd`
- Use command `systeminfo`
- Check `hyper-v requirement`
- run `Windows PowerShell` as Administrator
- Use command `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All`
- Enter `Y` to have the computer restart to complete the installation 
- [Enable Hyper-v](https://learn.microsoft.com/en-us/windows-server/virtualization/hyper-v/get-started/Install-Hyper-V?tabs=powershell&pivots=windows)

**Eable devloper mode in Windows**

- Go to `Windows Setting` -> `Update & Security` -> `Developer Mode`
- Select 


**Install WSL 2**
- Run `Windows PowerShell` as Administrator
- use command `wsl --install -d Ubuntu-22.04`
> You can replace Ubuntu into Debian or whatever you want

**Setting WSL 2 for your Linux distros**
- open `Windows PowerShell`
- use command `wsl --set-default-version 2`
> WSL 2 

**Run WSL 2**
- open `Windows PowerShell`
- change dir to your `working directory`
- use command  `wsl`
> You can replace Ubuntu into Debian or whatever you have installed

**Run Vscode**

- use command `code .`

# Q&A
## **Q: WslRegisterDistribution failed with error: 0x8000000d**
**Step 1: Confirm WSL status and installed distributions**

Open PowerShell (non-admin) and run:
```powershell
wsl --list --verbose
wsl --version
```
If no distros appear, or the version command fails (only showing help text), move to Step 2.

**Step 2: Clean up partial installations**
A. Unregister any broken distro

If `wsl -l -v` lists a problematic distro (e.g., Ubuntu), run:

```powershell
wsl --unregister <DistroName>
```

This removes incomplete installs.

**Step 3: Reinstall WSL & distro**

see [InstallWSL](#install-wsl)


## Q:Error: 0x800701bc WSL 2 requires an update to its kernel component.

- Use command `wsl --update`

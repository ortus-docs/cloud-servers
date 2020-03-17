---
description: >-
  This page will show you how to mange your site using CommandBox and how to
  move files back and forth from your your development environment where ever
  that may be.
---

# Managing your web site

Now that you have a site running in the cloud you will want to customize it. Remember that SSH pem file you downloaded. That is going to allow you to go on the server and edit files. If you are on a windows platform like me. Here are some tools I strongly suggest that you get locally.

1. CommandBox. This tool will allow you to make files and remove them locally. If you so decide that you want to edit and add files directly on the EC2 instance this can be done using the default instance of CommandBox on the server.  [https://commandbox.ortusbooks.com/](https://commandbox.ortusbooks.com/)
2. VSCode the editor of choice, and the reason I say that is because it has so many useful extensions. [https://code.visualstudio.com/download](https://code.visualstudio.com/download)
3. WinSCP the default file manager tool for Windows. [https://winscp.net/eng/index.php](https://winscp.net/eng/index.php)

If you are using the Windows Package Manager [Chocolatey ](https://chocolatey.org/)you can download all of these from there.

Here is a script to download them in powershell. Save the script as anything.ps1. Remember where you saved it.  With PowerShell, you must make sure [Get-ExecutionPolicy](https://go.microsoft.com/fwlink/?LinkID=135170) is not Restricted. We suggest using `Bypass` to bypass the policy to get things installed or `AllSigned` for quite a bit more security.

* Run `Get-ExecutionPolicy`. If it returns `Restricted`, then run `Set-ExecutionPolicy AllSigned` or `Set-ExecutionPolicy Bypass -Scope Process`.

Go to the right corner of the dialog box below and copy this script and save it naming it whatever you like as long as the extension ends as \*.ps1

```text
#Install Chocolatey
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

#Assign Packages to Install
$Packages = 'commandbox',`
            'vscode',`
            'winscp'

#Install Packages
ForEach ($PackageName in $Packages)
{choco install $PackageName -y}
```

```text
PS> .\anything.ps1 (enter)
```

If your scripts successfully installed you should see a new desktop icon for VSCode. If you open a shell \( cmd, powershell, git bash \) and type box you should see that Commandbox is installed.


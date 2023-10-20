---
description: >-
  There are several great VSCode plugins in this extension called Remote
  Development. These plugins allow you to connect directly to your Ortus AWS
  instance from any platform and start developing.
---

# Connect with VSCode

## Getting Box Powers

Becoming a box hero is a fairly straight forward process:

Here is the link to install your Remote Development extension to VSCode. [https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)\
Once you have your extension installed you will need some assets to get started.

1. Windows Password
2. Public EC2 IP address
3. pem file location that you created when you built your EC2 instance

Next let's open VSCode. Hold this key combination Ctrl +Shift + P and type Config. You will see some options. Select Remote-SSH: Open Configuration File.... This will open a file for you that has been prefilled with this information. If IdentityFile is not there add it please. Replace EC2 Public IP in the hostname and IdentityFile. Give the real name and and location of the pem file. Copy your Windows Password to the clipboard. Now go to the bottom left corner of VSCode. You will see a green square. Hover your mouse over it. It should say "Open a remote window." Click the green square. Select Remote-SSH: Connect to Host... Select your Alias whatever you put in for Alias. It should open a dropdown box asking for the password for windows. Put in your password and hit the enter key. A new instance of VSCode will open. The green rectangle where you launched from should read "SSH:Alias-name."

{% code title="config" %}
```bash
Host alias
    HostName EC2 Public IP
    User Administrator
    IdentityFile    ssh -i ~/.ssh/created.pem Administrator@EC2-Public-IP
```
{% endcode %}

Now let's run this keyboard combination command Ctrl + Shift + E this will open the file explorer window where your web site files are on the EC2 instance. Click the "Open Folder" blue bar. It will try and send you to C:\Users\Administrator change to:

```bash
C:\imetpub\wwwroot
```

This is going to allow you to have direct access to the files on your EC2 instances. CommandBox is preloaded so you can create any views, handlers and things of that nature.

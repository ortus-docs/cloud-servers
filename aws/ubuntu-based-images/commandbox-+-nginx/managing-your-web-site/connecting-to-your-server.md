---
description: Connecting to your server with WinSCP or VSCode
---

# Connecting to your server

This page will walk you through connecting to your new server using the popular free software program WinSCP. I have a script for you to download on step 11 "[Managing your web site](./)" page. We will also take a look at an exciting VSCode extension called [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack). It allows you to SSH directly to the EC2 instance and map the remote folder in your local VSCode IDE.

### Connecting via WinSCP

* Run WinSCP
* In the Login dialog, click on the “New” button
* Click the "New Session" button
* Then click the "Advanced..." button

![Connect via WinSCP](../../../../.gitbook/assets/image%20%288%29.png)

* From this dialog select the SSH Authentication browse button to the right of the input box.

![SSU Authentication](../../../../.gitbook/assets/image%20%287%29.png)

* You will be given a file explorer box. Then select your pem file that you downloaded when you created your ec2. The prompt with look like this click ok.

![Convert PEM file to a PPK file](../../../../.gitbook/assets/image%20%2813%29.png)

* Click the ok button

![Final Connection Step](../../../../.gitbook/assets/image%20%2811%29.png)

* You have connected

![](../../../../.gitbook/assets/image%20%289%29.png)


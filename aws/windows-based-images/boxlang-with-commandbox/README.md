# BoxLang with CommandBox

This AMI image will create a running BoxLang server with CFML compatibility module for you. If you do not want a ColdBox site we will show you how to remove it and have your own site. The first step is to have an AWS account. If you do not have one go to this URL to learn how to create an \[AWS account.]\( [https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/))

Choose the **BoxLang with CommandBox for Windows** AWS AMI. Go to this URL and do a search for Ortus at the top of the screen [https://aws.amazon.com/marketplace/](https://aws.amazon.com/marketplace/) and look for "Ortus solutions, corp"

![Ortus Solutions AMIs](../../../.gitbook/assets/aws/boxlang-with-commandbox-windows/marketplace-overview.png)

Click the **View purchase options** to subscribe button

![Purchase options for Ortus Solutions AMI](../../../.gitbook/assets/aws/boxlang-with-commandbox-windows/purchase-options.png)

Configuration options for subscription. In this section you can choose to add options to your contract, if not, You can click on "Continue configuration" button.

![AMI subcription options](../../../.gitbook/assets/aws/boxlang-with-commandbox-windows/configuration-options.png)

You can configure your Ortus Soluction software version or region, if not, just click on "Continue to Launch" button.

![Ortus Solution software configuration](../../../.gitbook/assets/aws/boxlang-with-commandbox-windows/software-configurations.png)

In "Launch" section you can choose method to launch, for this case, We're going to use EC2 method.

![Instance launch method](../../../.gitbook/assets/aws/boxlang-with-commandbox-windows/launch-options.png)

This will take you to the "Choose an Instance Type." The default instance and AWS free tier selected is `m4.large`. Unless you need more resources keep it at this.
If You desire or You do not have Key pair, You can generate new ones in "Key pair (login)" section.
On the "Network settings" section under "Firewall (Security groups)". We need to make a couple of changes. First is to go to the source column and select **My IP** so that SSH and RDP will only be enabled for your IP address (**VERY IMPORTANT**). Next allow **HTTP** and **HTTPS**. You can edit VPC, Subnet and Public IP configuration.
On "Configure Storage" section. If you want to persist your files, then add a volume. If you do not need to persist the files, keep the defaults.

![Instance launch set up](../../../.gitbook/assets/aws/boxlang-with-commandbox-windows/ec2-options.png)

Select your running instance. This will open some tabs at the bottom of the page. Select the "Description" tab. Look to the right on the description tab and look for "Public DNS (IPv4)." To the right of this text is the DNS name. Copy that name and paste it in a browser. It should look something like this `ec2-{public_dns}.compute-1.amazonaws.com`.

![Instance view page](../../../.gitbook/assets/aws/boxlang-with-commandbox-windows/ec2-overview.png)

Paste that URL in a browser and you should see the default ColdBox site.

![Instance view page](../../../.gitbook/assets/aws/boxlang-with-commandbox-windows/site-running.png)

Connect to your EC2 instance using Remote Desktop Protocol (RDP) or SSH to perform the following commands for creating a new handler in ColdBox Sample Application

Change your current directory to `C:\inetpub\wwwroot` and run `box` command to launch CommandBox CLI

```shell
PS C:\Users\administrator> Set-Location C:\inetpub\wwwroot\
PS C:\inetpub\wwwroot> box
```

Now, you can update system dependencies typing `update --system`. create a new handler for testing using `coldbox create handler type=index name=helloFromBoxLangCloudServer` command

```shell
Welcome to CommandBox! 
CommandBox:wwwroot> coldbox create handler type=index name=helloFromBoxLangMiniServer 
 INFO   Created View [C:\inetpub\wwwroot\views\helloFromBoxLangMiniServer/index.cfm] 

 INFO   Created Handler [C:\inetpub\wwwroot\handlers\helloFromBoxLangMiniServer.cfc]

 INFO   Created Integration Spec [C:\inetpub\wwwroot\tests\specs\integration\helloFromBoxLangMiniServerTest.cfc] 

CommandBox:wwwroot>
```

![New handler in running](../../../.gitbook/assets/aws/boxlang-with-commandbox-windows/new-handler.png)

**ENJOY YOUR CLOUD SERVER!**






















Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

PS C:\Users\administrator> Set-Location C:\inetpub\wwwroot\
PS C:\inetpub\wwwroot> box

Checking to see if your CLI version is current... 
Getting stable versioning information from https://downloads.ortussolutions.com/ortussolutions/commandbox/box-repo.json 
Your version of CommandBox (6.2.0+00826) is already current (6.2.0). 

Checking to see if your system modules are current... 
Checking for outdated system dependencies, please wait...
╔════════════════════════════════╤════════════════╤═════════╤═════════╤═════════════════════════╗  
║ Package                        │ Installed      │ Update  │ Latest  │ Location                ║  
╠════════════════════════════════╪════════════════╪═════════╪═════════╪═════════════════════════╣  
║ contentbox-cli@^1.8.0-snapshot │ 1.8.0-snapshot │ 1.8.0+5 │ 1.8.0+5 │ /modules/contentbox-cli ║  
╚════════════════════════════════╧════════════════╧═════════╧═════════╧═════════════════════════╝  
Key: Update Available   Major Update Available


Found (1) Outdated  systemDependency 
* contentbox-cli

Run the 'update --system' command to update all the outdated dependencies to their latest version. 
Or use 'update {slug} --system' to update a specific dependency

   ______                                          ______
  / ____/___  ____ ___  ____ ___  ____ _____  ____/ / __ )____  _  __
 / /   / __ \/ __ `__ \/ __ `__ \/ __ `/ __ \/ __  / __  / __ \| |/_// /___/ /_/ / / / / / / / / / / / /_/ / / / / /_/ / /_/ / /_/ />  <
\____/\____/_/ /_/ /_/_/ /_/ /_/\__,_/_/ /_/\__,_/_____/\____/_/|_| (R)  v6.2.0+00826 
                                             We'll leave the light on for ya'
Welcome to CommandBox!CommandBox:wwwroot> 
CommandBox:wwwroot> coldbox create handler type=index name=helloFromBoxLangWithCommandBox  INFO   Created View [C:\inetpub\wwwroot\views\helloFromBoxLangWithCommandBox/index.cfm] 
 INFO   Created Handler [C:\inetpub\wwwroot\handlers\helloFromBoxLangWithCommandBox.cfc]
 INFO   Created Integration Spec [C:\inetpub\wwwroot\tests\specs\integration\helloFromBoxLangWithCommandBoxTest.cfc] 
CommandBox:wwwroot> 

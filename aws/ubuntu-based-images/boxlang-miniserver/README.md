# Boxlang MiniServer

This AMI image will create a running BoxLang server with CFML compatibility module for you. If you do not want a ColdBox site we will show you how to remove it and have your own site. The first step is to have an AWS account. If you do not have one go to this URL to learn how to create an \[AWS account.]\( [https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/))

Choose the **BoxLang MiniServer for Ubuntu** AWS AMI. Go to this URL and do a search for Ortus at the top of the screen [https://aws.amazon.com/marketplace/](https://aws.amazon.com/marketplace/) and look for "Ortus solutions, corp"

![Ortus Solutions AMIs](../../../.gitbook/assets/aws/boxlang-miniserver-with-nginx/marketplace-overview.png)

Click the **View purchase options** to subscribe button

![Purchase options for Ortus Solutions AMI](../../../.gitbook/assets/aws/boxlang-miniserver-with-nginx/purchase-options.png)

Configuration options for subscription. In this section you can choose to add options to your contract, if not, You can click on "Continue configuration" button.

![AMI subcription options](../../../.gitbook/assets/aws/boxlang-miniserver-with-nginx/software-subscription.png)

You can configure your Ortus Soluction software version or region, if not, just click on "Continue to Launch" button.

![Ortus Solution software configuration](../../../.gitbook/assets/aws/boxlang-miniserver-with-nginx/software-configuration.png)

In "Launch" section you can choose method to launch, for this case, We're going to use EC2 method.

![Instance launch method](../../../.gitbook/assets/aws/boxlang-miniserver-with-nginx/launch-options.png)

This will take you to the "Choose an Instance Type." The default instance and AWS free tier selected is `t2.medium`. Unless you need more resources keep it at this.\
If You desire or You do not have Key pair, You can generate new ones in "Key pair (login)" section.\
On the "Network settings" section under "Firewall (Security groups)". We need to make a couple of changes. First is to go to the source column and select **My IP** so that SSH and RDP will only be enabled for your IP address (**VERY IMPORTANT**). Next allow **HTTP** and **HTTPS**. You can edit VPC, Subnet and Public IP configuration.\
On "Configure Storage" section. If you want to persist your files, then add a volume. If you do not need to persist the files, keep the defaults.

![Instance launch set up](../../../.gitbook/assets/aws/boxlang-miniserver-with-nginx/ec2-settings.png)

Select your running instance. This will open some tabs at the bottom of the page. Select the "Description" tab. Look to the right on the description tab and look for "Public DNS (IPv4)." To the right of this text is the DNS name. Copy that name and paste it in a browser. It should look something like this `ec2-{public_dns}.compute-1.amazonaws.com`.

![Instance view page](../../../.gitbook/assets/aws/boxlang-miniserver-with-nginx/ec2-overview.png)

Paste that URL in a browser and you should see the default ColdBox site.

![Instance view page](../../../.gitbook/assets/aws/boxlang-miniserver-with-nginx/site-running.png)

SSH to your instance with following command `ssh -i "/path/to/your/private-key" ubuntu@ec2-{public\_dns}.compute-1.amazonaws.com` and create a handler.

```shell
[01:31 PM]-[otisnado@otisnado-ortushp]-[~]-
$ ssh ubuntu@18.234.132.18
ubuntu@ip-172-31-28-63:~$
```

Elevate to root user, change your current directory to `/web/coldbox-site/wwwroot` and run `box` command to launch CommandBox CLI

```shell
ubuntu@ip-172-31-28-63:~$ sudo su
root@ip-172-31-28-63:/home/ubuntu# cd /web/coldbox-site/wwwroot/
root@ip-172-31-28-63:/web/coldbox-site/wwwroot# box
```

Now, you can update system dependencies typing `update --system`. create a new handler for testing using `coldbox create handler type=index name=helloFromBoxLangCloudServer` command

```shell
Welcome to CommandBox! 
CommandBox:wwwroot> coldbox create handler type=index name=helloFromBoxlangMiniserverCloudServer
 INFO   Created View [/web/coldbox-site/wwwroot/views/helloFromBoxlangMiniserverCloudServer/index.cfm]

 INFO   Created Handler [/web/coldbox-site/wwwroot/handlers/helloFromBoxlangMiniserverCloudServer.cfc]

 INFO   Created Integration Spec [/web/coldbox-site/wwwroot/tests/specs/integration/helloFromBoxlangMiniserverCloudServerTest.cfc]

CommandBox:wwwroot>
```

![New handler in running](../../../.gitbook/assets/aws/boxlang-miniserver-with-nginx/site-new-handler.png)

**ENJOY YOUR CLOUD SERVER!**

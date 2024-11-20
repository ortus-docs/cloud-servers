# Lucee + Nginx

This AMI image will create a running Lucee site for you. If you do not want a ColdBox site we will show you how to remove it and have your own site. The first step is to have an AWS account. If you do not have one go to this URL to learn how to create an \[AWS account.]\( [https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/))

* Choose the **Lucee CFML Server (Ubuntu+Nginx+Tomcat)** AWS AMI. Go to this URL and do a search for Ortus at the top of the screen [https://aws.amazon.com/marketplace/](https://aws.amazon.com/marketplace/) and look for "Ortus solutions, corp"

![Ortus Solutions AMIs](../../../.gitbook/assets/new-console/general/ami-selection.png)

* Click the **View purchase options** to subscribe button

![Purchase options for Ortus Solutions AMI](../../../.gitbook/assets/new-console/ubuntu-ami/ami-purchase-options.png)

* Click the **accept terms** button.

![Accept terms for Ortus Solutions AMI](../../../.gitbook/assets/new-console/ubuntu-ami/ami-accept-terms.png)

* Configuration options for subscription. In this section you can choose to add options to your contract, if not, You can click on "Continue configuration" button.

![AMI subcription options](../../../.gitbook/assets/new-console/ubuntu-ami/ami-subscription-options.png)

* You can configure your Ortus Soluction software version or region, if not, just click on "Continue to Launch" button.

![Ortus Solution software configuration](../../../.gitbook/assets/new-console/ubuntu-ami/ami-configure-software.png)

* In "Launch" section you can choose method to launch, for this case, We're going to use EC2 method.

![Instance launch method](../../../.gitbook/assets/new-console/ubuntu-ami/ami-launch-method.png)

* On the "Name and tags" page. Let's add a tag. Click the add Tag. They should be Key=Name and Value=Ortus Lucee CFML engine 5.2.9.31 (Ubuntu Server 18.04 LTS) Resource type=Instances.

![Instance name and tags](../../../.gitbook/assets/new-console/ubuntu-ami/instance-name-tags.png)

* This will take you to the "Choose an Instance Type." The default instance and AWS free tier selected is `t3.micro`. Unless you need more resources keep it at this.&#x20;

![Instance type](../../../.gitbook/assets/new-console/ubuntu-ami/instance-type.png)

* If You desire or You do not have Key pair, You can generate new ones in "Key pair (login)" section. **SAVE IT IN A SECURE PLACE!**&#x20;

![Key pair creation for instance](../../../.gitbook/assets/new-console/ubuntu-ami/instance-keypair.png)

* On the "Network settings" section under "Firewall (Security groups)". We need to make a couple of changes. First is to go to the source column and select **My IP** so that SSH and RDP will only be enabled for your IP address (**VERY IMPORTANT**). Next allow **HTTP** and **HTTPS**. You can edit VPC, Subnet and Public IP configuration.

![Instance security group](../../../.gitbook/assets/new-console/ubuntu-ami/instance-sg.png)

* On "Configure Storage" section. If you want to persist your files, then add a volume. If you do not need to persist the files, keep the defaults.

![Instance storage](../../../.gitbook/assets/new-console/ubuntu-ami/instance-storage.png)

* On "Summary" section you can review general information about your instance, cancel operation, launch instance and also, you can generate AWS CLI commands to deploy EC2 instance with desired configuration.

![Instance Summay](../../../.gitbook/assets/new-console/ubuntu-ami/instance-summary.png)

* You are on the "Launch Status" page. Go to the bottom right and click the button labeled "View Instances."&#x20;

![Instance launch status](../../../.gitbook/assets/new-console/ubuntu-ami/instance-status.png)

* Select your running instance. This will open some tabs at the bottom of the page. Select the "Description" tab. Look to the right on the description tab and look for "Public DNS (IPv4)." To the right of this text is the DNS name. Copy that name and paste it in a browser. It should look something like this `ec2-{public_dns}.compute-1.amazonaws.com`.

![Instance view page](../../../.gitbook/assets/new-console/ubuntu-ami/instance-view.png)

* Paste that URL in a browser and you should see the default ColdBox site.

* SSH to your instance with following command `ssh -i "/path/to/your/private-key" ubuntu@ec2-{public\_dns}.compute-1.amazonaws.com`

* When you SSH to the instance the web root is /web/coldbox-site/wwwroot **RUN ``cd`` COMMAND WITH SUDO OR ``su`` TO ROOT USER**

Enjoy your servers!


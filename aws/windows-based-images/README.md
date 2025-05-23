# Windows Based Images

Create an EC2 instance from an Ortus BoxLang engine \(Windows Server 2019\) AMI \(Amazon Machine Image\).  We have created several Windows-based images to deploy your BoxLang or CFML applications with Compat CFML BoxLang Module.

| Images                        | Status                                          |
| ----------------------------- | ----------------------------------------------- |
| BoxLang MiniServer with IIS   | :white_check_mark:                              |
| BoxLang with CommandBox       | :white_check_mark:                              |

## Software and tools installed matrix

On every Ubuntu based Cloud Server you will find software or tools to achieve best experience with our solutions. This software include:

|**Tool name**|**Version installed**|**BoxLang Miniserver + IIS**|**BoxLang + CommandBox**|
|-------------|---------------------|------------------------------|---------------------------|
|CommandBox   |Latest stable version| :white_check_mark:           | :white_check_mark:        |
|BoxLang CFEngine (into CommandBox)|Latest version|:x:|:white_check_mark:|
|BoxLang Miniserver (As OS binary)|Latest version|:white_check_mark:|:x:|
|ColdBox Application|Latest|:white_check_mark:|:white_check_mark:|
|IIS|Latest stable version|:white_check_mark:|:x:|
|URL Rewrite|Latest stable version|:x:|:white_check_mark:|
|Application Request Routing|Latest stable version|:x:|:white_check_mark:|

Due these Cloud Servers are Windows Server 2019 based, you can follow this [link](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/microsoftwindowsserver.windowsserver?tab=Overview) to know more about base software running.

## Environment variables

|**Variable**|**Default value**|**Description**|
|-------------|-----------------|--------------|
|BOXLANG_HOME|`C:\boxlangHome`|Directory where BoxLang place configs and modules|
|COMMANDBOX_HOME|`C:\CommandBox`|Directory where CommandBox place configs and modules|
|BOXLANG_TARGET_VERSION| `1.0.0-rc.3` |BoxLang version installed and to be used for BoxLang|
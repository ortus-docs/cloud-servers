# Windows 2019 Based Images

Create an Azure Virtual Machine from an Ortus BoxLang with CommandBox \(Ubuntu Server 24.04 LTS\) Virtual Machine \(Azure VM\).  We have created several based Ubuntu based images.

| Images | Status |
| :--- | :--- |
| BoxLang Miniserver | :white_check_mark: |
| BoxLang with CommandBox | :white_check_mark: |

## Software and tools installed matrix

On every Ubuntu based Cloud Server you will find software or tools to achieve best experience with our solutions. This software include:

|**Tool name**|**Version installed**|**BoxLang Miniserver**|**BoxLang + CommandBox**|
|-------------|---------------------|------------------------------|---------------------------|
|CommandBox   |Latest stable version| :white_check_mark:           | :white_check_mark:        |
|BoxLang CFEngine (into CommandBox)|Latest version|:x:|:white_check_mark:|
|BoxLang Miniserver (As OS binary)|Latest version|:white_check_mark:|:x:|
|ColdBox Application|Latest|:white_check_mark:|:white_check_mark:|

Due these Cloud Servers are Windows Server 2019 based, you can follow this [link](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/microsoftwindowsserver.windowsserver?tab=Overview) to know more about base software running.

## Environment variables

|**Variable**|**Default value**|**Description**|
|-------------|-----------------|--------------|
|BOXLANG_HOME|`C:\boxlangHome`|Directory where BoxLang place configs and modules|
|COMMANDBOX_HOME|`C:\CommandBox`|Directory where CommandBox place configs and modules|
|BOXLANG_TARGET_VERSION|`latest`|BoxLang version installed and to be used for BoxLang|
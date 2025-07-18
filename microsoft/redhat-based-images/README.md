# Deploying BoxLang RedHat Cloud Servers

Create a Azure Virtual Machine from an Ortus BoxLang MiniServer \(RedHat 8\) Virtual Machine \(Azure Virtual Machine\).  We have created several RedHat based images.

|  | Images | Status |
| :--- | :--- | :--- |
|  | BoxLang Miniserver | :white_check_mark: |
|  | BoxLang with CommandBox | :white_check_mark: |

## Software and tools installed matrix

On every Ubuntu based Cloud Server you will find software or tools to achieve best experience with our solutions. This software include:

|**Tool name**|**Version installed**|**BoxLang Miniserver + Nginx**|**BoxLang with CommandBox**|
|-------------|---------------------|------------------------------|---------------------------|
|CommandBox   |Latest stable version| :white_check_mark:           | :white_check_mark:        |
|BoxLang CFEngine (into CommandBox)|Latest version|:x:|:white_check_mark:|
|BoxLang Miniserver (As OS binary)|Latest version|:white_check_mark:|:x:|
|ColdBox Application|Latest|:white_check_mark:|:white_check_mark:|

Due these Cloud Servers are RedHat 8 based, you can follow this [link](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/redhat.rh-rhel?tab=Overview) to know more about base software running.

## Environment variables

|**Variable**|**Default value**|**Description**|
|-------------|-----------------|--------------|
|BOXLANG_HOME|`/root/.boxlang`|Directory where BoxLang place configs and modules|
|COMMANDBOX_HOME|`/root/.commandbox`|Directory where CommandBox place configs and modules|
|BOXLANG_TARGET_VERSION|`latest`|BoxLang version installed and to be used for BoxLang|
|BVM_HOME| `/usr/local/boxlang`|BoxLang Version Manager home|

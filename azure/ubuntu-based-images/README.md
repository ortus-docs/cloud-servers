# Deploying Boxlang Ubuntu Cloud Servers

Create an Azure Virtual Machine from an Ortus Boxlang with CommandBox \(Ubuntu Server 24.04 LTS\) Virtual Machine \(Azure VM\).  We have created several based Ubuntu based images.

|  | Images | Status |
| :--- | :--- | :--- |
|  | Boxlang with CommandBox | :white_check_mark: |
|  | Boxlang Miniserver + Nginx | :white_check_mark: |

## Software and tools installed matrix

On every Ubuntu based Cloud Server you will find software or tools to achieve best experience with our solutions. This software include:

|**Tool name**|**Version installed**|**Boxlang Miniserver + Nginx**|**Boxlang with CommandBox**|
|-------------|---------------------|------------------------------|---------------------------|
|CommandBox   |Latest stable version| :white_check_mark:           | :white_check_mark:        |
|Boxlang CFEngine (into CommandBox)|Latest version|:x:|:white_check_mark:|
|Boxlang Miniserver (As OS binary)|Latest version|:white_check_mark:|:x:|
|ColdBox Application|Latest|:white_check_mark:|:white_check_mark:|
|Nginx as HTTP Reverse Proxy|Latest stable version|:white_check_mark:|:x:|

Due these Cloud Servers are Ubuntu 24.04 LTS based, you can follow this [link](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/canonical.ubuntu-24_04-lts?tab=overview) to know more about base software running.

## Environment variables

|**Variable**|**Default value**|**Description**|
|-------------|-----------------|--------------|
|BOXLANG_HOME|`/root/.boxlang`|Directory where Boxlang place configs and modules|
|COMMANDBOX_HOME|`/root/.commandbox`|Directory where CommandBox place configs and modules|
|BOXLANG_TARGET_VERSION|1.0.0-rc.1|Boxlang version installed and to be used for Boxlang|

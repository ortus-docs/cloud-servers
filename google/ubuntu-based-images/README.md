# Deploying BoxLang Ubuntu Cloud Servers

Create a Google Cloud Virtual Machine from an Ortus BoxLang MiniServer \(Ubuntu 24.04 LTS\) Virtual Machine \(Google Compute Engine\).  We have created several Ubuntu based images.

|  | Images | Status |
| :--- | :--- | :--- |
|  | BoxLang MiniServer | :white_check_mark: |
|  | BoxLang with CommandBox | :white_check_mark: |

## Software and tools installed matrix

On every Ubuntu based Cloud Server you will find software or tools to achieve best experience with our solutions. This software include:

|**Tool name**|**Version installed**|**BoxLang MiniServer**|**BoxLang with CommandBox**|
|-------------|---------------------|------------------------------|---------------------------|
|CommandBox   |latest| :white_check_mark:           | :white_check_mark:        |
|BoxLang runtime|latest|:white_check_mark:(As OS binary)|:white_check_mark:(Into CommandBox)|
|BoxLang MiniServer (As OS binary)|latest|:white_check_mark:|:x:|
|ColdBox Application|Latest|:white_check_mark:|:white_check_mark:|

Due these Cloud Servers are Ubuntu 8 based, you can follow this [link](https://cloud.google.com/compute/docs/images/os-details#ubuntu_lts) to know more about base software running.

## Environment variables

|**Variable**|**Default value**|**Description**|
|-------------|-----------------|--------------|
|BOXLANG_HOME|`/root/.boxlang`|Directory where BoxLang place configs and modules|
|COMMANDBOX_HOME|`/root/.commandbox`|Directory where CommandBox place configs and modules|
|BOXLANG_TARGET_VERSION|`latest`|BoxLang version installed and to be used for BoxLang|
|BVM_HOME| `/usr/local/boxlang`|BoxLang Version Manager home|

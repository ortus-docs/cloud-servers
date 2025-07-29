# Deploying BoxLang Windows Cloud Servers

Create a Google Cloud Virtual Machine from an Ortus BoxLang MiniServer \(Windows 2019\) Virtual Machine \(Google Compute Engine\).  We have created several Windows based images.

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
|ColdBox Application|latest|:white_check_mark:|:white_check_mark:|

Due these Cloud Servers are Windows 2019 based, you can follow this [link](https://cloud.google.com/compute/docs/images/os-details#windows_server) to know more about base software running.

## Environment variables

|**Variable**|**Default value**|**Description**|
|-------------|-----------------|--------------|
|BOXLANG_HOME|`/root/.boxlang`|Directory where BoxLang place configs and modules|
|COMMANDBOX_HOME|`/root/.commandbox`|Directory where CommandBox place configs and modules|
|BOXLANG_TARGET_VERSION|`latest`|BoxLang version installed and to be used for BoxLang|
|BVM_HOME| `/usr/local/boxlang`|BoxLang Version Manager home|

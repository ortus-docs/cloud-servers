# Deploying BoxLang Windows Cloud Servers

Create a Google Cloud Virtual Machine from an Ortus BoxLang MiniServer \(Windows 2019\) Virtual Machine \(Google Compute Engine\).  We have created several Windows based images.

|  | Images | Status |
| :--- | :--- | :--- |
|  | BoxLang MiniServer | :white_check_mark: |
|  | BoxLang with CommandBox | :white_check_mark: |

## Software and tools installed matrix

On every Windows based Cloud Server you will find software or tools to achieve best experience with our solutions. This software include:

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

## Default site
For every Windows based BoxLang Cloud Server a scheduled task is used to get up and running a Web Server on well know HTTP port 80/TCP. You can find this scheduled task as name **"Start ColdBox Sample Application"**, depending of the server flavor this can be started using BoxLang MiniServer or CommandBox. If you want to start your any custom site, you can update this task if need it, or just only place your custom site under `C:\inetpub\wwwroot` folder

|Server|Command execution|Scheduled task name|
|:-----|:----------------|:------------------|
|BoxLang MiniServer|`C:\boxlang\bin\boxlang-miniserver.bat --host 0.0.0.0 --port 80 --webroot C:\inetpub\wwwroot --rewrites index.cfm`|Start ColdBox Sample Application|
|BoxLang with CommandBox|`C:\box\box.exe -commandbox_home=C:/CommandBox server start serverConfigFile="C:\inetpub\wwwroot\server.json"`|Start ColdBox Sample Application|

{% hint style="info" %}
If you only place your custom site under `C:\inetpub\wwwroot` remember to delete their content before in order to remove the sample ColdBox Application
{% endhint %}

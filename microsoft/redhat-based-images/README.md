# Deploying BoxLang Red Hat Cloud Servers

Create a Azure Virtual Machine from an Ortus BoxLang MiniServer \(Red Hat 8\) Virtual Machine \(Azure Virtual Machine\).  We have created several Red Hat based images.

|  | Images | Status |
| :--- | :--- | :--- |
|  | BoxLang MiniServer | :white_check_mark: |
|  | BoxLang with CommandBox | :white_check_mark: |

## Software and tools installed matrix

On every Re Hat based Cloud Server you will find software or tools to achieve best experience with our solutions. This software include:

|**Tool name**|**Version installed**|**BoxLang MiniServer**|**BoxLang with CommandBox**|
|-------------|---------------------|------------------------------|---------------------------|
|CommandBox   |latest| :white_check_mark:           | :white_check_mark:        |
|BoxLang runtime|latest|:white_check_mark:(As OS binary)|:white_check_mark:(Into CommandBox)|
|BoxLang MiniServer (As OS binary)|latest|:white_check_mark:|:x:|
|ColdBox Application|latest|:white_check_mark:|:white_check_mark:|

Due these Cloud Servers are Red Hat 8 based, you can follow this [link](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/redhat.rh-rhel?tab=Overview) to know more about base software running.

## Environment variables

|**Variable**|**Default value**|**Description**|
|-------------|-----------------|--------------|
|BOXLANG_HOME|`/root/.boxlang`|Directory where BoxLang place configs and modules|
|COMMANDBOX_HOME|`/root/.commandbox`|Directory where CommandBox place configs and modules|
|BOXLANG_TARGET_VERSION|`latest`|BoxLang version installed and to be used for BoxLang|
|BVM_HOME| `/usr/local/boxlang`|BoxLang Version Manager home|

## Default site
For every Linux based BoxLang Cloud Server a Systemd daemon is used to get up and running a Web Server on well know HTTP port 80/TCP. Depending of the server flavor this can be started using BoxLang MiniServer or CommandBox. If you want to start a custom site or application, you can update this daemon service if need it, or just only place your custom site or application under `/web/boxlang-site/wwwroot` directory.

|Server|Red Hat like|Debian like|Daemon name|
|:-----|:-----------|:----------|:----------|
|BoxLang MiniServer|`boxlang-miniserver --host 0.0.0.0 --port 80 --webroot /web/boxlang-site/wwwroot --rewrites index.cfm`|`boxlang-miniserver --host 0.0.0.0 --port 80 --webroot /web/boxlang-site/wwwroot --rewrites index.cfm`|boxlang-miniserver|
|BoxLang with CommandBox|`/bin/box server start serverConfigFile=server.json`|`/usr/local/bin/box server start serverConfigFile=server.json`|coldbox-site|

{% hint style="info" %}
If you only place your custom site under `/web/boxlang-site/wwwroot` remember to delete their content before in order to remove the sample ColdBox Application
{% endhint %}

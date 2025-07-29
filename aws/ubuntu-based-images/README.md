# Ubuntu Based Images

Create an EC2 instances from an Ortus BoxLang engine \(Ubuntu Server 24.04 LTS\) AMI \(Amazon Machine Image\).  We have created several based Ubuntu based images.

| Images                        | Status                                          |
| ----------------------------- | ----------------------------------------------- |
| BoxLang MiniServer            | :white_check_mark:                              |
| BoxLang with CommandBox       | :white_check_mark:                              |

## Software and tools installed matrix

On every Ubuntu based Cloud Server you will find software or tools to achieve best experience with our solutions. This software include:

|**Tool name**|**Version installed**|**BoxLang Miniserver + Nginx**|**BoxLang with CommandBox**|
|-------------|---------------------|------------------------------|---------------------------|
|CommandBox   |Latest stable version| :white_check_mark:           | :white_check_mark:        |
|BoxLang CFEngine (into CommandBox)|Latest version|:x:|:white_check_mark:|
|BoxLang Miniserver (As OS binary)|Latest version|:white_check_mark:|:x:|
|ColdBox Application|Latest|:white_check_mark:|:white_check_mark:|

Due these Cloud Servers are Ubuntu 24.04 LTS based, you can follow this [link](https://aws.amazon.com/marketplace/pp/prodview-s4zvkzmlirbga?sr=0-5&ref_=beagle&applicationId=AWSMPContessa) to know more about base software running.

## Environment variables

|**Variable**|**Default value**|**Description**|
|-------------|-----------------|--------------|
|BOXLANG_HOME|`/root/.boxlang`|Directory where BoxLang place configs and modules|
|COMMANDBOX_HOME|`/root/.commandbox`|Directory where CommandBox place configs and modules|
|BOXLANG_TARGET_VERSION| `latest` |BoxLang version installed and to be used for BoxLang|
|BVM_HOME| `/usr/local/boxlang`|BoxLang Version Manager home|
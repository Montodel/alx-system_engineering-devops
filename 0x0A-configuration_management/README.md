# 0x0A. Configuration management

project description ...

## Resources
* [Intro to Configuration Management](https://www.digitalocean.com/community/tutorials/an-introduction-to-configuration-management)
* [Resource Type: file](https://www.puppet.com/docs/puppet/5.5/types/file.html#file-providers)


## Project Overview
- [Mandatory Task](#mandatory-task)
	- [0. Create a file](0-create_a_file.pp)
	- [1. Install a package](1-install_a_package.pp)
	- [2. Execute a command](2-execute_a_command.pp)
- [Advanced Task](#advanced-task)
	- [Task - 013](link_to_fiel)
	- [Task - 014](link_to_fiel)

## Tasks
### Mandatory Task

#### 0. Create a file

**Problem:** Using Puppet, create a file in /tmp.

**Requirements:**
* File path is `/tmp/school`
* File permission is `0744`
* File owner is `www-data`
* File group is `www-data`
* File contains `I love Puppet`

```
imitor＠excalibur»alx-system_engineering-devops/0x0A-configuration_management(master)➜ sudo puppet apply 0-create_a_file.pp                                  (↻ 19?)
Notice: Compiled catalog for excalibur in environment production in 0.01 seconds
Notice: /Stage[main]/Main/File[/tmp/school]/ensure: defined content as '{md5}f1b70c2a42a98d82224986a612400db9'
Notice: Applied catalog in 0.01 seconds
imitor＠excalibur»alx-system_engineering-devops/0x0A-configuration_management(master)➜                           
imitor＠excalibur»~✗ cat /tmp/school                                                                                                3.10.7
I love Puppet% 
```
- [x] [0-create_a_file.pp](0-create_a_file.pp)

#### 1. Install a package

**Problem:** Using Puppet, install `flask` from `pip3`.

**Requirements:**
* Install `flask`
* Version must be `2.1.0`

```
imitor＠excalibur»alx-system_engineering-devops/0x0A-configuration_management(master)✗ puppet apply 1-install_a_package.pp
Notice: Compiled catalog for excalibur in environment production in 0.22 seconds
Notice: /Stage[main]/Main/Package[flask]/ensure: created
Notice: Applied catalog in 2.44 seconds
imitor＠excalibur»alx-system_engineering-devops/0x0A-configuration_management(master)➜ 
imitor＠excalibur»~➜ flask --version                                                                                                3.10.7
Python 3.8.16
Flask 2.1.0
Werkzeug 2.2.2
imitor＠excalibur»~➜                                                                                                                3.10.7
```
- [x] [1-install_a_package.pp](1-install_a_package.pp)

#### 2. Execute a command

**Problem:** Using Puppet, create a manifest that kills a process named killmenow.

**Requirements:**
* Must use the exec Puppet resource
* Must use pkill

```
Terminal #0 - starting my process

root@d391259bf577:/# cat killmenow
#!/bin/bash
while [[ true ]]
do
    sleep 2
done

root@d391259bf577:/# ./killmenow

Terminal #1 - executing my manifest

imitor＠excalibur»alx-system_engineering-devops/0x0A-configuration_management(master)➜ puppet apply 2-execute_a_command.pp         (↻ 20?)

Notice: Compiled catalog for excalibur in environment production in 0.02 seconds
Notice: /Stage[main]/Main/Exec[killmenow]/returns: executed successfully
Notice: Applied catalog in 0.03 seconds
imitor＠excalibur»alx-system_engineering-devops/0x0A-configuration_management(master)➜   

Terminal #0 - process has been terminated
imitor＠excalibur»alx-system_engineering-devops/0x0A-configuration_management(master)➜ ./killmenow                        
[1]    125865 terminated  ./killmenow
```
- [x] [2-execute_a_command.pp](2-execute_a_command.pp)

### No Advanced Task

# Install-Nexus
## overview
Sonatype Nexus is one of the best open-source artifact management tools. It is some tool that you cannot avoid in your CI/CD pipeline. It effectively manages deployable artifacts.

## Sonatype Nexus System Requirements
* Minimum 1 VCPU & 2 GB Memory
* Server firewall opened for port 22 & 8081
* OpenJDK 8
* All Nexus processes should run as a non-root nexus user.

## steps
* Update the yum packages
* Install OpenJDK 1.8
* allow firewall ports 8081
* Download the latest nexus
* Untar the downloaded file
* Rename the untared file to nexus 
* Create a new user named nexus to run the nexus service
* Change the ownership of nexus files and nexus data directory to nexus user
* Copy nexus.rc to /opt/nexus/bin/nexus.rc
* Copy nexus.service to /etc/systemd/system/nexus.service
* Enabel and restart nexus service

## Getting Started
* Run ansible playbook
```
 ansible-playbook nexus.yaml
```
* Visit the following url` http://your_node_ip:8081 `
* Log in using default username `admin`  and password found in `opt/sonatype-work/nexus3/admin.password`

### your url get response
![CHEESE!](file:///home/el-nabawy/Pictures/Screenshots/Screenshot%20from%202023-04-17%2003-01-24.png)

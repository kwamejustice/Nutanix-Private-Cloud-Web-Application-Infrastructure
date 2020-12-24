# Nutanix-Private-Cloud-Web-Application-Infrastructure

In accordance with stakeholders need for the task requested to perform as summarized below,

A 3-tier application stack with database devlopment VMs and production VMs needs to be built and a protection policy creation for the production environment. Workload expansion test with the addition of 1GB VCPU and 2GB memory to the development environment. And a full restortion of a deleted VM critical to production and a full restoration.

A setup of managed production envirornment network  (VLAN 0)and umanaged developmental network (VLAN 101) with network ip of 172.31.0.0/24 for managed and network ip of 172.31.101.0/24 for umanaged network. the maanged network IP should start with 172.31.0.210 amd end with 172.31.0.230

Microsoft SQL on windows should be used to build the database environment while CentOS Linux distro should be used for the production environment, with a NTP server configuration using the public pool service pool.ntp.org and 8.8.8.8 for Domain name servie. An image conatiner should be created with the Windows and CentOS images provided, with an initail build of 1GB VCPU and 4GB RAM for all servers. 




As per the Service Level Agreement with the customer these task where performed for HCI cluster proof of concept.


An image container was created with the Windows and Centos disk images
The domain name service was set to 8.8.8.8 and ntp was set using the public service pool.ntp.org
Three VMs were created respectively for the application production environment, database development environment and the webserver production environment
The managed network had a VLAN ID of 0 with production environment as its name and the umanaged network with a VLAN ID 0f 101 with development environment as is name
All VMs were created with 1 VCPU and 4 GB RAM 
The db-dev  servers VCPU were increasedy 1GB and memory was increased by 2 GB after the creation
The managed network was set on 172.31.0/24 with a gateway of 172.31.0.1 with an IP pool starting 172.31.0.210 and ending with 172.31.0.230
Data protection for the production environment was initiated and app-prod-1 server was deleted and restored successfully. The protection policy (protection-policy-for-production-env) hasno more than an hour of data loss after failure. 
The data base VMs uses the Windows OS and the production servers uses the Linux CentOs distro.

As per the directive the HCI cluster is ready for a demo.

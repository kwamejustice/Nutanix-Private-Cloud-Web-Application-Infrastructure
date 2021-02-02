# Nutanix-Private-Cloud-Web-Application-Infrastructure


## As per the Service Level Agreement with the customer these task where performed for HCI cluster proof of concept.


- An image container was created with the Windows and Centos disk images
- The domain name service was set to 8.8.8.8 and ntp was set using the public service pool.ntp.org

      ## Three VMs were created respectively for:
      The application production environment
      Database development environment 
      The webserver production environment
       
      The managed network had a VLAN ID of 0 with production environment as its name and the umanaged network 
      with a VLAN ID 0f 101 with development environment as is name
      
- All VMs were created with 1 VCPU and 4 GB RAM 
- The db-dev servers were virtically scaled with VCPU 1GB increase and memory increament by 2 GB after the creation
- The managed network was set on 172.31.0/24 with a gateway of 172.31.0.1 with an IP pool starting 172.31.0.210 and ending with 172.31.0.230
- Data protection for the production environment was initiated and app-prod-1 server was deleted and restored successfully.
         ## The protection policy (protection-policy-for-production-env) has no more than an hour of data loss after failure. 
- The data base VMs uses the Windows OS and the production servers uses the Linux CentOs OS.


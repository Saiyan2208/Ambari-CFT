# Ambari-CFT
The Ambari.json CFT code installs Ambari on a single node cluster. To increase the number of nodes, simply add more EC2 instances in the resources section of the CFT.

I have used **Centos 7** as the Linux Version. So make the necessary changes if you are using any other distribution. It is generally recommended to use **RHEL/Centos** or its distributions for Ambari.
The CFT sets up **Passwordless SSH** between the nodes in the clustes and starts the **ambari-server and ambari-agent**. The only manual effort required is to start all the services once the ambari-server starts and all the resources are up.

## CFT Walkthrough:

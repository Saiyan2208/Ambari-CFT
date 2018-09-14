# Ambari-CFT
The Ambari.json CFT code installs Ambari on a single node cluster. To increase the number of nodes, simply add more EC2 instances in the resources section of the CFT.

I have used **Centos 7** as the Linux Version. So make the necessary changes if you are using any other distribution. It is generally recommended to use **RHEL/Centos** or its distributions for Ambari.
The CFT sets up **Passwordless SSH** between the nodes in the clustes and starts the **ambari-server and ambari-agent**. The only manual effort required is to start all the services once the ambari-server starts and all the resources are up.

## CFT Walkthrough:

A single **ssh-keygen** key-pair is used for bidirectional passwordless authentication between all the nodes. The ssh keys are stored in a **S3-bucket**, from where the instance pulls the keys and adds them in their **.ssh/authorized_keys** file.

All these commands have been written in the **UserData** section of the CFT. Also all the ports required for differenr Hadoop services like 8000,8080,8441, etc have been taken care of in the **SecurityGroups** part of the CFT. 

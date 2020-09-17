# DR Rackware Deployment
## Step 1: Import RMM Image from Rackware
1.	Navigate to <a href="https://cloudmarketplace.oracle.com/marketplace/en_US/homePage.jspx" target="_blank">Oracle Marketplace</a>
2.	Search "Rackware" and select the "Rackware Migration Manager (RMM)
![](./screenshots/rmm-market.PNG)
3.	Click "Get App" and sign into your OCI Console
![](./screenshots/oci-sign.PNG)
4.	Launch the instance in the target compartment (This should be the same compartment as the one that will contain the instances of the migrated servers.)
![](./screenshots/launch.png)
5.	Enter a Name for the instance.\
    a.	dr_rackware_rmm
6.	Give the instance a shape appropriate for your deployment.
7.   In the ‘Add SSH Keys’ either upload your ssh key to connect to the instance after it is created or paste the key contents
    ![](./screenshots/add-ssh-keys.png)

## Step 2: Configure Rackware Components
Use the following **[guide](https://www.rackwareinc.com/rackware-rmm-oracle-marketplace-dr-march-2020)** to complete the Rackware deployment configuration. (Use the passthrough method)

## Step 3: Connect to the Backup database
1. Start an ssh connection to the newly created instance.
2. Navigate to the root compartment and edit the *defaults.xml* file
```
opc@<target-machine>$ sudo su -
root@<target-machine>$ vi /home/oracle/conf/ords/defaults.xml
```
3. Change the db.hostname entry to relfect the IP of the backup database
![](./screenshots/defaults-db.PNG)

4. Update the db.hostname in *ords_params.properties* file to reflect the IP of the backup database
```
root@<target-machine>$ vi /home/oracle/params/ords_params.properties
```
![](./screenshots/params-db.PNG)
5. Start the ORDS server on the target machine
```
root@<target-machine>$ sudo su - oracle
oracle@<target-machine>$ ./start_ords.sh
```

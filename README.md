# DR Rackware Deployment
## Step 1: Import RMM Image from Rackware
1.	Navigate to <a href="https://cloudmarketplace.oracle.com/marketplace/en_US/homePage.jspx" target="_blank">Oracle Marketplace</a>[Oracle Marketplace](https://cloudmarketplace.oracle.com/marketplace/en_US/homePage.jspx)
2.	Search "Rackware" and select the "Rackware Migration Manager (RMM)
![](./screenshots/rmm-market.PNG)
3.	Click "Get App" and sign into your OCI Console
![](./screenshots/oci-sign.png)
4.	Launch the instance in the target compartment (This should be the same compartment as the one that will contain the instances of the migrated servers.)
![](./screenshots/launch.png)
5.	Enter a Name for the instance.\
    a.	dr_rackware_rmm
6.	Give the instance a shape appropriate for your deployment.
7.   In the ‘Add SSH Keys’ either upload your ssh key to connect to the instance after it is created or paste the key contents
    ![](./screenshots/add-ssh-keys.png)

## Step 2: Configure Rackware Components
Use the following **[guide](https://www.rackwareinc.com/rackware-rmm-oracle-marketplace-dr-march-2020)** to complete the Rackware deployment configuration. (Use the passthrough method)

## Step 3: 

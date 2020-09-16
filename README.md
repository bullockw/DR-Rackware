# DR-Rackware
## Step 1: Import RMM Image from Rackware
1.	Log in to your OCI account
2.	Open the navigation menu. Under Core Infrastructure, go to Compute
3.	Select your target region
4.	Select your target compartment
5.	Click Custom Images.
6.	Click Import Image.

In the Create in Compartment list, select the compartment that you want to import the image to.   This should be the same compartment as the one that will contain the instances of the migrated servers. 

7.	Enter a Name for the image.
a.	rackware-rmm
8.	Select  Linux for the Operating System:
9.	Select “Import from an Object Storage URL”, then cut/paste the following into the Object Storage URL field
  a.	https://objectstorage.us-phoenix-1.oraclecloud.com/p/W_bmd4vwKpmm1wsrbgvXzKpW6SR6C7JCbKII2QCLDVs/n/a501635/b/templates/o/RMM-7-3-0-493-base
10.	In the Image Type section, select the format of the image.
  a.	OCI

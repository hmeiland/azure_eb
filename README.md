EasyBuild scripts for AzureHPC

These script assume you are running using the OpenLogic:CentOS-HPC:7.6:latest image, which includes the Mellanox OFED.

RPMs have been created from these scripts and can be used with the following repo file:

```
[azurehpc]
name=Azure HPC Repository
baseurl=https://yumrepohpc.blob.core.windows.net/$web
enabled=1
gpgcheck=0
```



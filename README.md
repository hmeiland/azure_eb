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

These RPMs assume you will be using /apps as the path for the applications; also you need to install Lmod and set the MODULEPATH to be able to use the software, e.g.:

```
sudo yum install -y Lmod
export MODULEPATH=/apps/modules/all:$MODULEPATH
```

for convinience you can put the export in your .bashrc file.


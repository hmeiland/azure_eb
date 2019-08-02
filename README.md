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
for convinience you can put the export in your .bashrc file or in the central /etc/bashrc.

To install the compiler toolchain of GCC and OpenMPI (Mellanox optimised including ucx, hcoll and mxm)
```
sudo yum install gompi-2019a-hpcx
```
and with the AzureHB (AMD Epyc Naples) optimised OpenBLAS, FFTW and ScaLAPACK:
```
sudo yum install foss-2019a-AzureHB
```
Or go directly for a optimized application (for now just HPL :) )
```
sudo yum install HPL-2.3-foss-2019a-AzureHB
```

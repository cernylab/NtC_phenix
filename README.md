Installation for phenix-1.19.2-4158

tar -zxvf phenix-installer-1.19.2-4158-intel-linux-2.6-x86_64-centos6.tar.gz  
cd ./phenix-installer-1.19.2-4158-intel-linux-2.6-x86_64-centos6  
./install —prefix=/PHENIX/INSTALLATION/DIRECTORY  
cd /PHENIX/INSTALLATION/DIRECTORY/phenix-1.19.2-4158  
cp /PATH/TO/phenix-1.19.2-4158-NtCInstallerPatch-v3.patch .  
patch -p0 -i ./phenix-1.19.2-4158-NtCInstallerPatch-v3.patch  
cd ./build  
shopt -s extglob  
rm -- !(config_modules.sh)  
./config_modules.sh  
source setpaths.sh  
libtbx.scons -j 8  

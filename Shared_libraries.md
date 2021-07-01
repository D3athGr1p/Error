#### Error : apt: error while loading shared libraries: libapt-private.so.0.0: cannot open shared object file: No such file or directory

```javaascipt

Ok at first find out what is your distribution. In my case:
lsb_release -a 
No LSB modules are available. 
Distributor ID: Ubuntu 
Description: Ubuntu 18.04.3 LTS 
Release: 18.04 Codename: bionic
Then visit and download ".deb" file to your PC accordingly:
Next run command sudo dpkg -i <XYZ>.deb . In my case:
sudo dpkg -i apt_1.6.1_amd64.deb
Then you just need to do:
apt --fix-broken install

Reference link:
https://stackoverflow.com/questions/59560633/unable-to-use-apt-or-apt-get-with-the-error-message

```
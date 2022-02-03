1. install plugin digital ocean
```
vagrant plugin install vagrant-digitalocean
```
2. add box-dummy
```
vagrant box add digital_ocean https://github.com/smdahlen/vagrant-digitalocean/raw/master/box/digital_ocean.box
```
3. init
```
vagrant init
```
4. rsa -> copy on vagrantfile
```
ssh-keygen -t rsa
```
5. up
```
vagrant up –provider=digital_ocean
```
refrensi
https://blog.eduonix.com/system-programming/learn-use-vagrant-cloud/
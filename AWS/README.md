1. install plugin aws
```
vagrant plugin install vagrant-aws
```
2. add box-dummy
```
vagrant box add dummy https://github.com/mitchellh/vagrant-aws/raw/master/dummy.box
```
3. init
```
vagrant init
```
4. up
```
vagrant up --provider=aws
```
refrensi
https://blog.eduonix.com/system-programming/learn-use-vagrant-cloud/
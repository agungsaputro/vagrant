1. install on local
```
export CLOUD_SDK_REPO="cloud-sdk-$(lsb_release -c -s)"

echo "deb http://packages.cloud.google.com/apt $CLOUD_SDK_REPO main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list

curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -

sudo apt-get update && sudo apt-get install google-cloud-sdk
```
2. install plugin 
```
vagrant plugin install vagrant-google
```
3. enable SSH a public key
```
gcloud compute project-info add-metadata --metadata-from-file \
  sshKeys=/tmp/id_rsa.pub
```
4. add the box specific to Google
```
vagrant box add gce https://github.com/mitchellh/vagrant-google/raw/master/google.box
```
5. up
```
vagrant up –provider=google
```


refrensi
https://blog.eduonix.com/system-programming/learn-use-vagrant-cloud/
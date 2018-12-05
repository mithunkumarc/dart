# dart

installation : https://www.techomoro.com/how-to-install-and-setup-flutter-on-ubuntu-18-04-1-lts-bionic-beaver/


for server side : dart installation : 

link : https://www.dartlang.org/tools/sdk

$ sudo apt-get update
$ sudo apt-get install apt-transport-https

$ sudo sh -c 'curl https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -'

$ sudo sh -c 'curl https://storage.googleapis.com/download.dartlang.org/linux/debian/dart_stable.list > /etc/apt/sources.list.d/dart_stable.list'

$ sudo apt-get update

$ sudo apt-get install dart


for current session : run 
$ export PATH="$PATH:/usr/lib/dart/bin"


for global session : 
              
              open file : bashrc
              sudo nano ~/.bashrc
              export PATH="$PATH:/usr/lib/dart/bin"       
              
              save and exit

---

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

#### flutter installation on ubuntu 18.04



        // creating dedicatetd android folder
        mitun@mithun-Latitude-E6230:~$ cd android

        //extracting flutter to android folder
        mitun@mithun-Latitude-E6230:~/android$ tar xf ~/Downloads/flutter_linux_v1.0.0-stable.tar.xz 
        mitun@mithun-Latitude-E6230:~/android$ pwd
        /home/mitun/android
        mitun@mithun-Latitude-E6230:~/android$ cd\
        > 

        //add flutter path in bash profile
        mitun@mithun-Latitude-E6230:~$ sudo nano ~/.bashrc


          add this line : export PATH=/home/mitun/android/flutter/bin:$PATH

          //ctrl + save, exit

        //activate 
        mitun@mithun-Latitude-E6230:~$ source /home/mitun/.bashrc

        //check path
        mitun@mithun-Latitude-E6230:~$ echo $PATH
       
       
        flutter need git:
        sudo apt update
        sudo apt install git
        git --version
        
        //run flutter command to test
        >>flutter 
        
        download android studio, add dart and flutter plugins. goto settings select plugins to search





---

#### web development : dart with html

      https://webdev.dartlang.org/guides/get-started


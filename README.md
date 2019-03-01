# java-ballerina-installation


##  Install Java8

    1.  mkdir /usr/lib/jvm
    
    2.  cd /usr/lib/jvm
    
    3.  wget -c --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.tar.gz
    
    4.  gzip -d jdk-8u131-linux-x64.tar.gz
    
    5.  tar xvf jdk-8u131-linux-x64.tar
    
    6.  vi /etc/environment
    
    7.  Add the paths - /usr/lib/jvm/jdk1.8.0_131/bin:/usr/lib/jvm/jdk1.8.0_131/db/bin:/usr/lib/jvm/jdk1.8.0_131/jre/bin 
    
    8.  vi ~/.bashrc - Add : export JAVA_HOME=/usr/lib/jvm/jdk1.8.0_131

    9.  update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jdk1.8.0_131/bin/java" 0
    
    10. update-alternatives --install "/usr/bin/javac" "javac" "/usr/lib/jvm/jdk1.8.0_131/bin/javac" 0
    
    11. update-alternatives --set java /usr/lib/jvm/jdk1.8.0_131/bin/java
    
    12. update-alternatives --set javac /usr/lib/jvm/jdk1.8.0_131/bin/javac
    
    13. Verify - 
    
        a.  update-alternatives --list java
        
              /usr/lib/jvm/jdk1.8.0_131/bin/java
              
        b.  update-alternatives --list javac
        
              /usr/lib/jvm/jdk1.8.0_131/bin/javac
              
    14. Reboot terminal
    
    
##  Install Ballerina 

    1.  mkdir -p /var/lib/ballerina ; cd /var/lib/ballerina
    
    2.  wget https://product-dist.ballerina.io/downloads/0.990.3/ballerina-0.990.3.zip
    
    3.  unzip ballerina-0.990.3.zip 
    
    4.  vi /var/lib/ballerina/ballerina-0.990.3/bin/ballerina 
    
    5.  Add : JAVA_HOME=/usr/lib/jvm/jdk1.8.0_131
    
    6.  vi ~/.bashrc and add the below variables 
    
        export PATH=$PATH:/var/lib/ballerina/ballerina-0.990.3/bin
        
        export BALLERINA_HOME=/var/lib/ballerina/ballerina-0.990.3/

    7.  source ~/.bashrc 
    
    8.  Verify -
    
        ballerina --version
        
            Ballerina 0.990.3

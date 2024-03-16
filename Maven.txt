Maven Installation - Amazon Linux 2023 ( Latest Version ) 

1.login into EC2 Instance 
2.Change the directory to cd /opt folder 
3.Run wget https://dlcdn.apache.org/maven/maven-3/3.9.6/binaries/apache-maven-3.9.6-bin.tar.gz - check before executing as it may be updated in apache maven official installation page.
4.Run tar -xvfz "filename" #tar filename that you got into your folder by running above cmd.
5.Change name to maven using mv apache-maven-3.9.6 maven
6.Change Directory to bin folder using cd /maven/bin and copy path of bin folder using pwd cmd
7.Copy path of maven ( /maven )
8.Change the directory to home(~) and run sudo yum install java-11-amazon-corretto-devel and sudo yum install java-11-amazon-corretto-jmods (if required)
9.Can check Installation of java by using cmds, java --version and javac
10. modify .bash_profile file in (~) Directory. Include below details. 
#below details
JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto.x86_64
M2_HOME=/opt/maven
M2=/opt/maven/bin
# User specific environment and startup programs

PATH=$PATH:$HOME/bin:$JAVA_HOME:$M2_HOME:$M2
#upto here.
11. save it using escape + :wq!
12. now you can check by running mvn --version and can run any maven cmds from anyfolder where you have java files to compile,test and package. 

Note: Remember! User that you assumed in terminal while deploying maven and modifying files. If you try to run mvn cmds with another user you end in problem mvn not found. 


 


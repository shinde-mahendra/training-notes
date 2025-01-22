# Introduction

-  Jenkins is a popular 'automation' tool used for implementing devop workflows.
-  Jenkins itself is based on another existing tool called `hudson`.
-  Written in Java, supported on any platform that supports java (Java SE and EE)

## Installation 

1. Download jenkins from https://jenkins.io

   Note:
   1.  Download LTS Version of "Generic War"
   2.  In Virtual Lab, `jenkins.war` can be found in `c:\` pre-downloaded.
  
2. Start CMD and Goto directory which contains `jenkins.war`

    ```cmd
    cd \
    dir jenkins*  
    java -jar jenkins.war
    ```
3.  After Jenkins is launched the CMD would keep the process running.

    > DO NOT CLOSE COMMAND PROMPT
    
1.  You should get `Initial Password` in command prompt. Select and copy it.

    > NEVER USE `CTRL_C` to copy as in Command prompt `CTRL+C` is used to STOP Process
    > Instead use Right Click of mouse to copy

1.  Visit `http://localhost:8080` with web browser.

    > DO NOT USE MS Internet Explorer, Use MS Edge Web browser

1.  Provide the Initial password and click to continue
1.  Jenkins post installation setup, now would give you TWO choices
    - Install Suggested Plugin [Default]
    - Select Plugins Install [ Not Recommended ] 
1.  Create the `Admin User` for jenkins 
1.  Click `Save and continue` -> click `Save and Finish` -> Start using Jenkins


## Explore the Jenkins Home Directory

- Jenkins is installed in `User Home Directory` with name `.jenkins`
   - On Windows Machines => C:\Users\AzureAdmin\.jenkins
   - ON Linux Machines   => /home/AzureAdmin/.jenkins
   - ON MachOS           => /Users/AzureAdmin/.jenkins

- Jenkins Home directory structure

```cmd
cd \Users\AzureAdmin\.jenkins
tree
```
> You can also use `Windows Explorer` to explore Jenkins Home directory

## Prepare Jenkins for building Java Project 

1. Log-in into Jenkins
1. Goto `Manage Jenkins` -> `Tools`
1. Goto `JDK Installations`, Click on `Add JDK`
    - Name : Java17
    - JAVA_HOME:   C:\Program Files\Java\jdk-17
1. Scroll down for `Maven Installations`
1. Click on `Add Maven` button
1. Enter name as `M2` and **uncheck** `Install Automatically`
1. Set MAVEN_HOME to `C:\apache-maven-3.9.7`
1. Click on `Save` 

## Stop Jenkins [Unsafe]
1. Logout [Optional]
2. Goto command prompt where `Jenkins process` is running, and use `CTRL+C` to stop.

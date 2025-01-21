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
1.  Provide the Initial password and click to continue
1.  Jenkins post installation setup, now would give you TWO choices
    - Install Suggested Plugin [Default]
    - Select Plugins Install [ Not Recommended ] 
1.  Create the `Admin User` for jenkins 
2.  Click `Save and continue` -> click `Save and Finish` -> Start using Jenkins
3.  


    

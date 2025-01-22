# Jenkins Free style Job

## Demo 1

1. Login into Jenkins with Admin User
1. Goto Jenkins Dashboard (Use Top Left Corner Logo of Jenkins)
1. Click on "New Item" in left side navigation panel.

  ```yml 
  Item-Name: Job1
  Item-Type: Freestyle project
  ```
1. Click Ok to start creating a new job
1. Using left side navigation panel, goto "General" and enter description for the project `Sample Job`
1. Using left side navigation panel, goto "Build Steps"
1. Click on `Add Build Step` then choose `Execute Windows Batch Command`
1. Enter the command

   ```cmd
   echo "Hello World"
   ```
1.  Click on `Save` button
1.  Now try to `Run` the job at least three times.
1.  Jenkins Dashboard -> Job1 -> In left side panel, there should LIST OF BUILDs
1.  Now, using windows explorer, explore the folder `C:\Users\AzureAdmin\.Jenkins\Jobs\job1`

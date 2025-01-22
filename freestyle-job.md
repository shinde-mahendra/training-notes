# Jenkins Free style Job
A Jenkins freestyle job is a type of project that allows you to define a sequence of steps to perform a task, such as building or deploying a project. It provides a flexible and straightforward way to configure and manage your automation processes.

## Key Features

- **Build Steps**: Define a series of steps to execute, such as shell commands, batch scripts, or invoking other build tools like Maven or Gradle.
- **Post-Build Actions**: Configure actions to perform after the build, such as archiving artifacts, sending notifications, or triggering other jobs.
- **Source Code Management (SCM)**: Integrate with version control systems like Git, Subversion, or Mercurial to fetch the source code for your project.
- **Build Triggers**: Set up triggers to start the job automatically, such as polling the SCM, scheduling builds, or responding to webhooks.
- **Build Environment**: Configure the environment for the build, including setting environment variables, using custom workspace locations, or throttling concurrent builds.
- **Parameters**: Define parameters to make your job configurable, allowing you to pass different values for each build.

## Configuration Options

- **General**: Set job description, discard old builds, and enable the job as parameterized.
- **Source Code Management**: Configure the SCM settings to fetch the source code.
- **Build Triggers**: Set up triggers to initiate the build process.
- **Build Environment**: Specify environment settings for the build.
- **Build Steps**: Define the steps to execute during the build process.
- **Post-Build Actions**: Configure actions to perform after the build completes.

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

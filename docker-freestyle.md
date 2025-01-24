# Build Docker images using Freestyle project

1. Login into cloud based jenkins instance
   Visit `http://20.197.17.42/` and use username `mahendra` and password `Password@1234`
2. Click on `New Item` -> Select Project Type `Freestyle Project` and enter project name as `Docker-YOURNAME`
3. Goto `Source Code Management` choose `Git` and then provide this GitHub repository URL
   `https://github.com/shinde-mahendra/ci-servlet-demo`
4.  Goto `Build Steps` -> Choose `Build / Publish Docker Image` then enter `Image name` as `mahendra2515/YOURNAME`

    > Kindly replace YOURNAME with your name in lower letters.
5.  Click on `Save` button and then `Build Now`. Check if your build is successful.
6.  Goto `Jenkina Manager` > `Credentials` > `System` > `Global Credentials (unrestricted)`
7.  Click on `docker-id` and view docker username and password (Password is concealed)
8.  Go back to `Dashboard` of jenkins, select the project/job created in step #2. Then click `Configure` button.
9.  Scroll down to `Build/Publish Docker image` step.
10.  Check/Enable `Push Image` and then for Registry credentials choose `docker-id`
11.  Check/Enable `Clean local images` and then `Save` the changes.
12.  Click `Build Now` button to start the job.

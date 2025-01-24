# Build Docker images using Freestyle project

1. Login into cloud based jenkins instance
   Visit `http://20.197.17.42/` and use username `mahendra` and password `Password@1234`
2. Click on `New Item` -> Select Project Type `Freestyle Project` and enter project name as `Docker-YOURNAME`
3. Goto `Source Code Management` choose `Git` and then provide this GitHub repository URL
   `https://github.com/shinde-mahendra/ci-servlet-demo`
4.  Goto `Build Steps` -> Choose `Build / Publish Docker Image` then enter `Image name` as `mahendra2515/YOURNAME`

    > Kindly replace YOURNAME with your name in lower letters.
5.  Click on `Save` button and then `Build Now`. Check if your build is successful.

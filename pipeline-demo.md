# Pipeline Demo : building java application


1. Create new `Pipeline` Job in Jenkins
2. Scroll down for Pipeline, and then use following Pipeline script:

```groovy
pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M2"
    }

    stages {
        stage("checkout"){
            steps{
                cleanWs()
                git url: 'https://github.com/mahendra-shinde/webgoat', branch: 'main'
            }
        }
        stage('Build') {
            steps {
               bat "mvn  clean package"
            }

            post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
                }
            }
        }
    }
}
```
3. Save the pipeline job and then try `Build Now`
4. After build is completed, click on `Build Id` and then click `Pipeline Overview`

# Declarative Pipelines

Jenkins Declarative Pipelines are a way to define and control continuous integration/continuous delivery (CI/CD) processes using a scripted pipeline syntax that is easier to read and maintain. Declarative Pipelines provide a more structured approach compared to the older Scripted Pipelines.

### Key Features of Declarative Pipelines:

- **Pipeline Definition**: Written in a Jenkinsfile which is stored in the source control repository.

- **Structure**: Uses a more readable and structured syntax.

- **Stages and Steps**: Divides the pipeline into stages (major phases) and steps (individual tasks within stages).

- **Built-in Error Handling**: Automatically handles errors and allows defining specific actions for post-pipeline completion.

### Example
```groovy
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Add build steps here
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Add test steps here
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add deploy steps here
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
```

### Components:

- pipeline {}: Top-level block defining the pipeline.

- agent {}: Specifies where the pipeline should run.

- stages {}: Groups the stages of the pipeline.

- stage {}: Defines individual stages within the pipeline.

- steps {}: Contains the individual tasks to perform in each stage.

- post {}: Defines actions to take after the pipeline completes (e.g., cleanup, notifications).

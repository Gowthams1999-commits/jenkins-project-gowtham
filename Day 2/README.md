# Multi-Stage and Multi-Agent Jenkins Pipeline

## This template explains how to set up multiple stages and multiple agents in a single Jenkinsfile.

In this example, we use `agent none` to prevent defining a global agent. This allows you to define multiple agents inside individual stages.

### Example:

```groovy
pipeline {
    agent none  // This means no global agent is defined.

    stages {
        stage('Node.js Application') {
            agent {
                docker 'node:latest'  // Use the Node.js Docker image for this stage
            }
            steps {
                sh 'node -v'  // Run 'node -v' command to check if Node.js is installed
            }
        }

        stage('MySQL') {
            agent {
                docker 'mysql:latest'  // Use the MySQL Docker image for this stage
            }
            steps {
                sh 'echo "my mysql"'  // Placeholder command for MySQL
            }
        }
    }
}


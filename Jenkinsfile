pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ('Build') {
            steps {
                echo "Building the application"
            }
        }
        stage ('Sonar') {
            steps {
                echo "Executing Sonar Scans"
            }
        }
        stage ('DockerBuildNPush') {
            steps {
                echo "Building and pushing docker images"
            }
        }
        stage ('Devenv') {
            steps {
                echo "Deploying our application to dev"
            }
        }
        stage ('Testenv') {
            steps {
                echo "Deploying our application to test"
            }
        }
    }
}

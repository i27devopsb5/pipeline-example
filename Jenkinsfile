pipeline {
    agent {
        label 'java-slave'
    }
    environment {
        DOCKER_CREDS = credentials('i27devopsb4_dockerhub_creds') // username and passowrd
    }
    stages {
        stage('DockerBP'){
            steps {
                echo "Depoying from main branch"
            }
        }
    }
}

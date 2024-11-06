pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage('DockerBP'){
            steps {
                //nginx pull, change the name to myownname and push to my registry 
                docker pull nginx
            }
        }
    }
}

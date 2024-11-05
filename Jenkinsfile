pipeline {
    agent any
    tools {
        maven 'Maven_3.8.8' // this name should match to the name creted under tool section
    }
    stages {
        stage('MavenVersion') {
            steps {
                echo "Welcome to Tools demo"
                sh 'mvn --version'
            }
        }
    }
}

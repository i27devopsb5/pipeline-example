pipeline {
    agent {
        label 'java-slave'
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

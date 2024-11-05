pipeline {
    agent {
        label 'java-slave' // k8s-slave //node-slave
    }
    stages {
        stage('build') {
            steps {
                echo "Executing Build Block"
                sh 'hostname -i'
            }
        }
        stage ('Sonar') {
            steps {
                echo "Executing Sonar Block"
            }
        }
        // stage ('docker') {
        //     agent {
        //         label 'docker-slave'
        //     }
        //     steps {
        //         sh 'docker pull nginx'
        //     }
        // }
    }
}

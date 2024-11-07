pipeline {
    agent {
        label 'java-slave'  
    }
    parameters{
        choice(name: 'deployToProd',
               choices: 'no\nyes',
               description: 'Deploy to Production?'
            )   

    }
    stages {
        stage('Build') {
            steps {
                echo 'Building the application'
            }
        }
        stage ('deploytoProd') {
            when {
                expression {
                    params.deployToProd == 'yes'
                }
            }
            steps {
                echo 'Deploying to Production'
            }
        }
    }
}

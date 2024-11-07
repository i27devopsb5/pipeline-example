pipeline {
    agent {
        label 'java-slave'
    }
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage ('Build') {
            steps {
                echo 'Building the project..'
            }
        }
        stage ('sonar') {
            steps {
                echo 'Running sonar scan..'
            }   
        }
        stage ('Deploy to Dev') {
            steps {
                echo 'Deploying to Dev..'
            }
        }
        stage ('Deploy to QA') {
            steps {
                echo 'Deploying to QA..'
            }
        }
        stage('Deploy to Stage Env') {
            when {
                expression {
                    BRANCH_NAME == /(production|staging)/
                }
            }
            steps {
                echo 'Deploying to Stage..'
            }
        }
    }
}

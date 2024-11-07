pipeline {
    agent {
        label 'java-slave'
    }
    environment {
        DEPLOY_TO = 'somename'
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
                    branch 'main'
                }
            }
            steps {
                echo 'Deploying to Stage..'
            }
        }
        stage('Deploy to Prod') {
            when {
                anyOf {
                    branch 'prodbranch'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo 'Deploying to Prod..'
            }
        }
    }
}

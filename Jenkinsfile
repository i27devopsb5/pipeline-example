pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ('Build') {
            steps {
                echo 'Building the project..'
            }
        }
        stage ('Scans') {
            parallel {
                stage ('Sonar') {
                    steps {
                        echo 'Running sonar scan..'
                        sleep 10  
                    }
                }
                stage ('checkmarx') {
                    steps {
                        echo 'Running checkmarx scan..'
                        sleep 10
                    }

                }
                stage ('fortify') {
                    steps {
                        echo 'Running fortify scan..'
                        sleep 10
                    }
                }
            }
        }
        stage ('Deploy') {
            steps {
                echo 'Deploying the project..'
            }
        }
    }
}

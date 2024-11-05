pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ('Build') {
            steps {
                retry (3) {
                    echo "Welcome to Jenkins Pipeline"
                    error "I will print error message"
                }
                echo "Message: After 3 times"

            }
        }
    }
}

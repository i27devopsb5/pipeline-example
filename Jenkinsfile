pipeline {
    agent {
        label 'java-slave'
    }

    environment { // Super 
        NAME = "siva"
        COURSE = "k8s"
    }

    stages {
        stage ('FirstStage') {
            environment {
                CLOUD = "GCP"
                NAME = "Meghana"
            }
            steps {
                echo "Welcome ${NAME}"
                echo "You enrolled for ${COURSE} Course"
                echo "You are certified in ${CLOUD}"
            }
        }
    }
}

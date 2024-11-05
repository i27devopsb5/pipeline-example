pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ("Hello") {
            steps {
                // actual steps 
                echo "hello world"
                sh 'date'
                echo "executing my first stage"
            }
        }
        stage('scriptblock') {
            steps {
                script {
                    // my script 
                    // define a variable 
                    def course = "k8s"
                    if (course == "k8s")
                      println("Thanks for enrolling in ${course}")
                      // ${variable} , ${env.variable}, ${pipelineparams}
                    else 
                      println("Do learn ${course}")
                }
            }
        }
    }
}

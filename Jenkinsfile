pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage('DockerBP'){
            steps {
                //nginx pull, change the name to myownname and push to my registry 
                sh "docker pull nginx"
                echo "********************* Printing images Before changing the tag ******************"
                sh "docker images"
                sh "docker tag nginx i27devopsb4/nginx:b5"
                echo "********************* Printing images After changing the tag ******************"
                sh "docker images"
                echo "********************** Pushing the Image to Repo ******************"
                sh "docker push i27devopsb4/nginx:b5"
            }
        }
    }
}

pipeline {
    //agent { dockerfile true }
     //args '--entrypoint=\'\''
    agent {
        dockerfile {
            args '--entrypoint=\'\''
        }
    }
    /*stages {
        stage('Test') {
            steps {
                //sh 'java -version'
                //sh 'docker images' 
                echo "hello from the other side"
            }
        }
    }*/
    stages {
        stage('Build image') {
            steps {
                echo 'Starting to build docker image'

                script {
                    def customImage = docker.build("my-image:${env.BUILD_ID}")
                    customImage.push()
                }
            }
        }
    }
}

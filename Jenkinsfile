pipeline {
    //agent { dockerfile true }
     //args '--entrypoint=\'\''
    agent {
        dockerfile {
            args '--entrypoint=\'\''
        }
    }
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
    stages {
       stage('Test') {
           steps {
               //sh 'java -version'
               //sh 'docker images' 
               echo "hello from the other side"
               sh ' docker run --rm -u root -p 8080:8080 -v jenkins-data:/var/jenkins_home -v $(which docker):/usr/bin/docker -v /var/run/docker.sock:/var/run/docker.sock -v "$HOME":/home jenkinsci/blueocean'
            }
        }
    }
}

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
            }
        }
    }
}

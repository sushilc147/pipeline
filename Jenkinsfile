pipeline {
    //agent { dockerfile true }
     //args '--entrypoint=\'\''
    agent {
        dockerfile {
            args '--entrypoint=\'\''
        }
    }
    stages {
        stage('Test') {
            steps {
                //sh 'java -version'
                echo "hello from the other side"
            }
        }
    }
}

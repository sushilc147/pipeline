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
                //sh 'docker images' 
                echo "hello from the other side"
                
         stage('Initialize'){
                def dockerHome = tool 'myDocker'
                env.PATH = "${dockerHome}/bin:${env.PATH}"
              steps {
                 sh 'docker images'
                 echo "==========x=========="
                  }
               }
            }
        }
    }
}

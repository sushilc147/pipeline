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
            }
        }
    }           
    stage('Initialize'){
         steps {   
            def dockerHome = tool 'myDocker'
            env.PATH = "${dockerHome}/bin:${env.PATH}"
             sh 'docker images'
             echo "==========x=========="
                  }
    }
}

// Jenkinsfile

pipeline {
  // Assign to docker slave(s) label, could also be 'any'
  agent {
    label 'master'
  }

  stages {
    stage('Docker node test') {
      agent {
        docker {
          // Set both label and image
          label 'master'
          image 'node:10-alpine'
          args '--user root'
        }
      }
      steps {
        echo '1234'
        //sh 'ls -lha'
        sh 'pwd'
        // Steps run in node:7-alpine docker container on docker slave
      }
    }
  }
} 

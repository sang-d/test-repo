// Jenkinsfile

pipeline {
  // Assign to docker slave(s) label, could also be 'any'
  agent {
    label 'BpaDocker' 
  }

  stages {
    stage('Docker node test') {
      agent {
        docker {
          // Set both label and image
          label 'BpaDocker'
          image 'node:7-alpine'
          args '--user root'
        }
      }
      steps {
        echo '1234'
        sh 'ls -lha'
        sh 'pwd'
        // Steps run in node:7-alpine docker container on docker slave
      }
    }
  }
} 

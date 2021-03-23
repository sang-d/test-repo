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
          image 'node:7-alpine'
        }
      }
      steps {
        echo '1234'
        ls -lha
        pwd
        // Steps run in node:7-alpine docker container on docker slave
      }
    }
  }
} 

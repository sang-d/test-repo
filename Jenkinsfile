// Jenkinsfile

pipeline {
  // Assign to docker slave(s) label, could also be 'any'
  agent {
    label 'any' 
  }

  stages {
    stage('Docker node test') {
      agent {
        docker {
          // Set both label and image
          label 'master'
          image 'python:3.7'
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

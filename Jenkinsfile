pipeline {
    agent { 
        node { label 'master'}
        docker 'python:3.7' 
    } 
    stages {
        stage('Example Build') {
            steps {
                echo '1234'
                sh 'ls -lha'
                sh 'pwd'
            }
        }
    }
}

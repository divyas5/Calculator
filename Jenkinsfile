pipeline {
    agent none
    stages {
        stage('Build') {
            agent {
                docker{
                   image 'python:3.8-alpine'
                }
              }
            
       steps {
                sh 'python -m py_compile myscript.py'
           stash(name: 'compiled-results', includes: '*.py*')
            }
            
        }
    }
}

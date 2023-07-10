pipeline {
  agent any
  stages {
    stage('Code Check') {
      steps {
        git(url: 'https://github.com/kydoblaster/JenkinzHello.git', branch: 'main')
      }
    }

    stage('Log') {
      parallel {
        stage('Log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front end unit test') {
          steps {
            sh '&& npm i && npm run test:unit'
          }
        }

      }
    }

  }
}
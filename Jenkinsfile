pipeline {
  agent any
  stages {
    stage('Code Check') {
      steps {
        git(url: 'https://github.com/kydoblaster/JenkinzHello.git', branch: 'main')
      }
    }

    stage('Log') {
      steps {
        sh 'ls -la'
      }
    }

    stage('Build') {
      steps {
        sh 'docker build .'
      }
    }

  }
}
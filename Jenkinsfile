pipeline {
  agent any
  stages {
    stage('Code Check') {
      steps {
        git(url: 'https://github.com/kydoblaster/JenkinzHello.git', branch: 'main')
      }
    }

    stage('List Contents in Log') {
      steps {
        sh 'ls -la'
      }
    }

  }
}
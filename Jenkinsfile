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
        sh 'docker build -f Dockerfile . -t longconsilvers'
      }
    }

    stage('log in') {
      environment {
        DOCKERHUB_USER = 'kydoblaster'
        DOCKERHUB_PASSWORD = '3Jedii327!!!'
      }
      steps {
        sh 'docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASSWORD'
      }
    }

    stage('Push') {
      steps {
        sh 'docker push longconsilvers:latest'
      }
    }

  }
}
pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
    stage('Deploy') {
      steps {
        sh 'mvn deploy'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
  }
}

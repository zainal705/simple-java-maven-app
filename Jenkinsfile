pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'mvn clean package'
          }
        }
        stage('') {
          steps {
            sh 'file 29'
          }
        }
      }
    }
    stage('Test') {
      post {
        always {
          junit 'target/surefire-reports/*.xml'

        }

      }
      steps {
        sh 'mvn test'
      }
    }
  }
  tools {
    maven 'maven'
    jdk 'jdk'
  }
}
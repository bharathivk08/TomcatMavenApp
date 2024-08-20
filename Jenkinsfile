pipeline {
  agent any
  stages {
    stage('Scm') {
      steps {
        git 'https://github.com/bharathivk08/TomcatMavenApp.git'
      }
    }

    stage('Build') {
      steps {
        bat 'mvn -Dmaven.test.failure.ignore=true clean package'
      }
    }

  }
  tools {
    maven 'MAVEN-3.9.8'
  }
  environment {
    env = 'staging'
  }
}
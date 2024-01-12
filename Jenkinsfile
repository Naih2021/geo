pipeline {
    agent any
tools {
  maven 'M2_HOME'
  }
    stages {
        stage('maven clean') {
            steps {
                sh 'mvn clean'
            }
        }
        stage('maven install') {
            steps {
                sh 'mvn install'
            }
        }
        stage('maven compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage ('maven test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('maven package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}

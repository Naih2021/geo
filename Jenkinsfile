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
        Stage('maven compile') {
            steps {
                sh 'mvn compile'
            }
        }
        Stage ('maven test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('maven package') {
            steps {
                sh 'mvn package'
            }
        }
        stage('maven sonar') {
            steps {
                sh 'mvn sonar:sonar'
            }
        }
    }
}

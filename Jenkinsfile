pipeline {
    agent any

    tools {
        maven 'M2_HOME'
    }

    stages {
        stage('Clean') {
            steps {
                sh 'mvn clean'
            }
        }

        stage('Install') {
            steps {
                sh 'mvn install'
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                script {
                    withSonarQubeEnv('SonarQube Server') {
                        sh 'mvn sonar:sonar'
                    }
                }
            }
        }
    }

    post {
        success {
            echo 'Build successful! Trigger additional steps here.'
        }
        failure {
            echo 'Build failed! Take necessary actions for failure.'
        }
    }
}

pipeline {
    agent any
    stages {
        stage('pre-build') {
            steps {
                sh 'chmod +x ./gradlew'
            }
        }
        stage('unit-test') {
            steps{
                sh './gradlew clean test --no-daemon'
            }
        }
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
            }
        }
        stage('DockerTest') {
            steps {
                echo 'Testing docker installation'
                sh 'docker ps -a'
            }
        }
    }
}

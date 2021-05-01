pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
            }
        }
        stage('pre-build') {
        sh 'chmod +x ./gradlew'
        }
    }
}

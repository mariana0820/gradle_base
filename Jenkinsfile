pipeline {
    agent any
    stages {
        stage('pre-build') {
            steps {
                sh 'chmod +x ./gradlew'
            }
        }
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
            }
        }
    }
}

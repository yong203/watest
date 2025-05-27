pipeline {
    agent any

    stages {
        stage('Prepare') {
            steps {
                // gradlew에 실행 권한 부여
                sh 'chmod +x gradlew'
            }
        }

        stage('Compile') {
            steps {
                sh './gradlew compileJava'
            }
        }

        stage('Build') {
            steps {
                sh './gradlew build'
            }
        }

        stage('Unit test') {
            steps {
                sh './gradlew test'
            }
        }
    }
}

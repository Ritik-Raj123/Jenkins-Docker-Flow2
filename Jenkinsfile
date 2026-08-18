pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                dir('frontend') {
                    bat 'npm install'
                }
            }
        }

        stage('Build') {
            steps {
                dir('frontend') {
                    bat 'npm run build'
                }
            }
        }

        stage('Deploy') {
            steps {
                bat 'xcopy /E /I /Y frontend\\dist F:\\CICD\\Deployment'
            }
        }

    }
}
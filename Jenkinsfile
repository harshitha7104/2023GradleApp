pipeline {
    agent any
    
    tools {
        gradle 'Gradle'
        jdk 'JDK'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/harshitha7104/2023GradleApp.git'
            }
        }

        stage('Build') {
            steps {
                sh 'gradle build'
            }
        }

        stage('Test') {
            steps {
                sh 'gradle test'
            }
        }

        stage('Run Application') {
            steps {
                sh 'gradle display'
            }
        }
    }

    post {
        success {
            echo 'Build and deployment successful'
        }
        failure {
            echo 'Build Failed'
        }
    }
}

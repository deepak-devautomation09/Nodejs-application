pipeline {
    agent any

    tools {
        nodejs "NodeJS 18"  // Make sure this name matches what you configured in Jenkins (Manage Jenkins > Global Tool Configuration)
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'  // Replace this if you use another test command
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'  // Optional: if your app has a build step
            }
        }
    }
}

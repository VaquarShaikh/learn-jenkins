pipeline {
    agent any
    stages {
        stage('git checkout') {
            steps {
                git credentialsId: 'a462d379-a01f-49b0-a074-9e1a9d579e0a', branch: 'main', url: 'https://github.com/VaquarShaikh/learn-jenkins.git'
            }
        }

        stage('install dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build nextjs') {
            steps {
                sh 'npm run build'
            }
        }
    }

    // post {
    //     always {
    //         cleanWs()
    //     }
    // }
}

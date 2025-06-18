pipeline {
    agent any

    tools {
        nodejs 'Node 24' // must match the name from Global Tool Config
    }

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
        failure {
            echo 'Something went wrong.'
        }
    }
}

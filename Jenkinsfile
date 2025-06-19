pipeline {
    agent any
    
    stages {
        stage('Install Dependencies') {
            steps {
                sh '/usr/local/bin/npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh '/usr/local/bin/npm test'
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

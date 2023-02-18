pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o out PES1UG20CS614.cpp'
                build job : 'PES1UG20CS614-1'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

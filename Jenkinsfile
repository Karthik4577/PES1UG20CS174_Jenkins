pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS174-1 PES1UG20CS174-1.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS174-1'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployed Successfully'
            }
        }
    }

    post {
        always {
            script {
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
    }
}

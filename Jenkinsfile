
pipeline {

    agent any

    stages {

        stage('Build') {

            steps {

                echo 'Building Application'

                sh 'python3 --version'
            }
        }
        stage('Install Dependencies') {
            steps{
                sh'''
                pip3 install --break-system-packages -r requirements.txt'''
            }
        }
            }
        }
        stage('Test') {

            steps {

                echo 'Running Tests'

                sh 'python3 -m pytest'
            }
        }
    }

    post {

        success {

            echo 'Build Successful'
        }

        failure {

            echo 'Build Failed'
        }

        always {

            echo 'Pipeline Finished'
        }
    }
}

pipeline {
    agent any

    environment {
        function_name = 'nithulambda'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building'
                sh 'mvn package'
            }
        }
        

        stage('Push') {
            steps {
                echo 'Push'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Build'
            }
        }
    }
}

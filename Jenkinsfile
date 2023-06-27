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

                sh "aws s3 cp target/sample-1.0.3.jar s3://nitu123s3"
            }
        }

        stage('Deploy') {
            steps {
                echo 'Build'

                sh "aws lambda update-function-code --function-name $function_name --s3-bucket nitu123s3 --s3-key sample-1.0.3.jar"
            }
        }
    }
}

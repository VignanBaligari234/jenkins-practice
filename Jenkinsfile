pipeline {
    agent { node { label 'AGENT-1' } }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                ls -ltr
                pwd
                echo "hello script"
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post { 
            always { 
                echo 'I will always run whether job is success or not'
            }
            success {
                echo 'i will run only if the job is success'
            }
            failure {
                echo 'I will run only when the job is failure'
            }
        }
}
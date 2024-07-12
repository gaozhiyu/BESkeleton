pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo " test value: ${params.'test'}"
            }
        }
        stage ('Invoke_pipeline') {
            steps {
                build job: 'firstpipeline'
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
}

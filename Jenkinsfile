pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            lockableResources {
                label('tredkopen')
                resourceNumber(1)
            }
            steps {
                echo 'Testing..'
                sleep 30
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

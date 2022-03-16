pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            lock(label: 'tredkopen', variable: 'var') {
                echo "Resource locked: ${env.var}"
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

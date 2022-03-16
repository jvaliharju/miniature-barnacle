pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                lock(resource: null, label: 'tredkopen', variable: 'var') {
                    echo "Resource locked: ${env.var}"
                }
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

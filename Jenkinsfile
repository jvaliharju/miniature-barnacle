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
                lock(resource: null, label: 'TRE OPEN', variable: 'var') {
                    echo "Resource locked: ${env.var}"
                    sleep 90
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

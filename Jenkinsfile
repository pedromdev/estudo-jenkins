pipeline {
    agent {
      docker {
        image 'node:7-alpine'
      }
    }

    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }

    stages {
        stage('build') {
            steps {
                sh 'npm --version'
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
                sh 'printenv'
            }
        }
    }
}

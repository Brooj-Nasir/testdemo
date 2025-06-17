pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    environment {
        MBL_VERSION = '1.3.0'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
                echo "Building version ${env.MBL_VERSION}"
                bat 'nvm install'
            }
        }
    }
}

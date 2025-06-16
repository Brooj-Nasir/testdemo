flag=true
pipeline {
    agent any
    tools {
        maven 'maven'
    }
    environment {
        // variables defined here can be used by any stage
        MBL_VERSION = '1.3.0'
    }
    stages {
        stage('build') {
            steps {
                echo 'Building Project'
                // using environment variable
                // To output the value of variable in string use " "
                echo "Building version ${MBL_VERSION}"
                sh 'mvn install'
            }
        }
    }
}

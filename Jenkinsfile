flag = true

pipeline {
    agent any
    parameters {
        // these are types of parameters
        string(name: 'VERSION', defaultValue: '', description: 'version to deploy on prod')
        choice(name: 'VERSION_CHOICE', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'Select version')
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run tests?')
    }

    environment {
        // variables defined here can be used by any stage
        NEW_VERSION = '1.3.0'
    }

    stages {
        stage('build') {
            steps {
                echo 'Building Project'
            }
        }

        stage('test') {
            when {
                expression {
                    params.executeTests
                }
            }
            steps {
                echo 'Testing Project'
            }
        }
    }
}

pipeline {
    agent any
    stages {
        stage('run frontend') {
            steps {
                echo 'executing yarn.....'
                nodejs('NodeJS 16.1.0') {
                    sh 'yarn install'
                }
            }
        }
        stage('run backend')
        steps {
            echo 'executing gradle....'
            withGradle() {
                sh './gradlew -v'
            }
        }

    }

}
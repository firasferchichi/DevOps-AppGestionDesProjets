pipeline {
    agent any
    triggers {
        pollSCM('H/2 * * * *')
    }

    tools {
        maven 'M2_HOME'
        jdk 'JAVA_HOME'
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Récupération du code depuis Git réussie.'
            }
        }
        
        stage('Compile') {
            steps {
                dir('backend') {
                    sh 'mvn compile'
                }
            }
        }
    }
}

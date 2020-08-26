



pipeline {
    agent any
    tools {
        maven 'M2_HOME'
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                sleep 5
            }
        }
             stage('build') {
            steps {
                echo 'Hello build'
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
                sleep 5
            }
        }
             stage('deploy') {
            steps {
                echo 'Hello deploy'
                sleep 5
            }
        }
           stage('test') {
            steps {
                echo 'Hello test'
                sleep 4
            }
        }  
    }
}






pipeline {
    agent any
    tools {
        maven 'M2_HOME'
    }
    triggers {
   pollSCM '* * * * *' 
        
    stages {
        
             stage('build') {
            steps {
                echo 'Hello build'
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
                
            }
        }
             stage('test') {
            steps {
                sh 'mvn test'
                
            }
        }
           stage('build and publish image') {
            steps {
                script {
              checkout scm
                    docker.withRegistrty('', 'dockerUserID') { 
              def customImage = docker.build("mvalerie2020/hol-pipeline:${env.BUILD_ID}") 
              def customImage1 = docker.build("mvalerie2020/hol-pipeline")
              customImage.push()
              customImage1.push()
          
            }
        }  
    }
}
                                             }
                                             }
                                             
                                             
                                             
                                             
                                             
                                             
                                             
                                             
                                             
                                             

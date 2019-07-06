pipeline {
  agent any 
    stages {
      stage('clone code'){
        steps {
        git 'https://github.com/amolmane123/maven-project.git'
        }
      }      
      stage('compile'){
        steps {
          withMaven(maven: 'maven'){
            sh 'mvn compile'
          }
        }
      }
    }  
}

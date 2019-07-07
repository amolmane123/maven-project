pipeline {
  agent any 
    stages {
      stage('clone code'){
        agent{label 'maven, '}
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
      
      stage('test') {
        steps {
          withMaven(maven: 'maven') {
            sh 'mvn test' 
          }
        }
      }
      
      stage('package') {
        steps {
          withMaven(maven: 'maven') {
            sh 'mvn package' 
          }
        }
      }
      
      stage('install') {
        steps {
          withMaven(maven: 'maven') {
            sh 'mvn install' 
          }
        }
      }
    }  
}

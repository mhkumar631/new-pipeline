pipeline {
    agents any
    
    stages {
        stage ('compile stage') {
           steps {
           WithMaven(maven : 'maven_3_5_0') {
              sh 'mvn clean compile'
              
            }
          }
       }
         stage ('Testing stage') {
            steps {
            WithMaven(maven : 'maven_3_5_0') {
              sh 'mvn test'
            }
          }
       }
       
         stage ('Deployment stage') {
            steps {
            WithMaven(maven : 'maven_3_5_0') {
              sh  'mvn deploy'
              
            }
          }
        }
    
       }


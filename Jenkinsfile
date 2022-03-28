pipeline{

 agent any
   
 environment {
       DOCKERHUB_CREDENTIALS= credentials('nexus')
                }     
 stages {

    stage('gitclone'){
        steps {
            git 'https://github.com/Sammouda23/python-app.git'
              }
        }
    stage('Build'){
        steps{
            sh 'docker build -t 20.231.74.68:9001/myphth-app:${BUILD_ID} . '
        } }   
    stage('Login'){
        steps{
           sh 'docker login --username admin -p admin 20.231.74.68:9001'
        }   }

    stage('Push'){
        steps{
            sh 'docker push  "20.231.74.68:9001/myphth-app:${BUILD_ID}" '
        }      

    }
    }
}

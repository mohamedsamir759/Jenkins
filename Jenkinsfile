 pipeline {
        agent any
        stages {
                stage('scm') {
                        steps {
                        git branch: 'main', url: 'https://github.com/mohamedsamir759/python-project.git'
                        }
                }
                stage('Build') {
                        steps {
                           script {
                                withDockerRegistry(credentialsId: 'dockerhub') {
                                sh "docker build -t mohamedsamir759/test:v1 ."
                                sh "docker push mohamedsamir759/test:v1 "
                                }
                
                           }   
                        }
                }
        }   
}        

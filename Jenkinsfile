pipeline {

    agent any
    stages {

        stage('Build') {

            steps {

                echo "Building.."

                sh '''

                cd myapp

                pip install -r requirements.txt --break-system-packages 

                '''

            }

        }

        stage('Test') {

            steps {

                echo "Testing.."

                sh '''

                cd myapp

                python3 hello.py

                python3 hello.py --name=Samir

                '''

            }

        }

        stage('Deliver') {

            steps {

                echo 'Deliver....'

                sh '''

                echo "doing delivery stuff.."

                '''

            }

        }

    }

}

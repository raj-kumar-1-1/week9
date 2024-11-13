pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                script {
                    bat 'docker build -t rajkumar121w9dhappcsedd .'
                     bat 'docker tag w9-csedd:latest rajkumar121/rajkumar121w9dhappcsedd:latest'
                      bat 'docker push rajkumar121/rajkumar121w9dhappcsedd:latest'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Run tests here if you have any
                    echo 'Running tests...'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                   //  Deploy your Docker image
                   bat 'minikube start'
                    bat 'kubectl apply -f deployment.yaml'
                   bat 'kubectl apply -f service.yaml'
                    bat 'minikube dashboard'
                    bat 'kubectl get services'
                    echo 'Deploying application...'
                }
            }
        }
    }
}

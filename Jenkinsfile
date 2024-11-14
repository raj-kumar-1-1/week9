pipeline {
    agent any 

    stages {
        // stage('Build') {
        //     steps {
        //         script {
        //             bat 'docker build -t week9 .'
        //              bat 'docker tag week9:latest rajkumar121/week9:latest'
        //               bat 'docker push rajkumar121/week9:latest'
        //         }
        //     }
        // }
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
                    bat 'kubectl apply -f my-kube1-deployment.yaml'
                   bat 'kubectl apply -f my-kube1-service.yaml'
                    bat 'minikube dashboard'
                    bat 'kubectl get services'
                    echo 'Deploying application...'
                }
            }
        }
    }
}

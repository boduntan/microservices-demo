pipeline {
    agent any

    environment {
        DOCKER_HUB_CREDENTIALS = credentials('dockeruser')
        AWS_ACCESS_KEY_ID = credentials('AWS_Access_Key')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_Secret_Key')
        
    }

    stages {
        //stage('Checkout') {
        //   steps {
        //        checkout scm
        //    }
        stage('Build adservice and push to dockerhub') {
            steps {
                script {
                    //build adservice
                    checkout scm
                    docker.build("thecodegirl/adservice:${env.BUILD_ID}", "-f /var/lib/jenkins/adservice/Dockerfile /var/lib/jenkins/adservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://hub.docker.com/', DOCKER_HUB_CREDENTIALS) {
                        docker.image("thecodegirl/adservice:${env.BUILD_ID}").push()
                        docker.image("thecodegirl/adservice:${env.BUILD_ID}").push('latest')
                    }
                }
            }
        }

        stage('Build cartservice and push to dockerhub') {
            steps {
                script {
                    //build adservice
                    checkout scm
                    docker.build("thecodegirl/cartservice:${env.BUILD_ID}", "-f /var/lib/jenkins/cartservice/src/Dockerfile /var/lib/jenkins/cartservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://hub.docker.com/', DOCKER_HUB_CREDENTIALS) {
                        docker.image("thecodegirl/cartservice:${env.BUILD_ID}").push()
                        docker.image("thecodegirl/cartservice:${env.BUILD_ID}").push('latest')
                    }
                }
            }
        }

        stage('Build checkoutservice and push to dockerhub') {
            steps {
                script {
                    //build adservice
                    checkout scm
                    docker.build("thecodegirl/checkoutservice:${env.BUILD_ID}", "-f /var/lib/jenkins/checkoutservice/Dockerfile /var/lib/jenkins/checkoutservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://hub.docker.com/', DOCKER_HUB_CREDENTIALS) {
                        docker.image("thecodegirl/checkoutservice:${env.BUILD_ID}").push()
                        docker.image("thecodegirl/checkoutservice:${env.BUILD_ID}").push('latest')
                    }
                }
            }
        }

        stage('Build currencyservice and push to dockerhub') {
            steps {
                script {
                    //build adservice
                    checkout scm
                    docker.build("thecodegirl/currencyservice:${env.BUILD_ID}", "-f /var/lib/jenkins/currencyservice/Dockerfile /var/lib/jenkins/currencyservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://hub.docker.com/', DOCKER_HUB_CREDENTIALS) {
                        docker.image("thecodegirl/currencyservice:${env.BUILD_ID}").push()
                        docker.image("thecodegirl/currencyservice:${env.BUILD_ID}").push('latest')
                    }
                }
            }
        }

        stage('Build emailservice and push to dockerhub') {
            steps {
                script {
                    //build adservice
                    checkout scm
                    docker.build("thecodegirl/emailservice:${env.BUILD_ID}", "-f /var/lib/jenkins/emailservice/Dockerfile /var/lib/jenkins/emailservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://hub.docker.com/', DOCKER_HUB_CREDENTIALS) {
                        docker.image("thecodegirl/emailservice:${env.BUILD_ID}").push()
                        docker.image("thecodegirl/emailservice:${env.BUILD_ID}").push('latest')
                    }
                }
            }
        }

        stage('Build frontend and push to dockerhub') {
            steps {
                script {
                    //build adservice
                    checkout scm
                    docker.build("thecodegirl/frontend:${env.BUILD_ID}", "--f /var/lib/jenkins/frontend/Dockerfile /var/lib/jenkins/frontend")

                    //push to docker hub
                    
                    docker.withRegistry('https://hub.docker.com/', DOCKER_HUB_CREDENTIALS) {
                        docker.image("thecodegirl/frontendservice:${env.BUILD_ID}").push()
                        docker.image("thecodegirl/frontend:${env.BUILD_ID}").push('latest')
                    }
                }
            }
        }

        stage('Build loadgenerator and push to dockerhub') {
            steps {
                script {
                    //build adservice
                    checkout scm
                    docker.build("thecodegirl/loadgenerator:${env.BUILD_ID}", "-f /var/lib/jenkins/loadgenerator/Dockerfile /var/lib/jenkins/loadgenerator")

                    //push to docker hub
                    
                    docker.withRegistry('https://hub.docker.com/', DOCKER_HUB_CREDENTIALS) {
                        docker.image("thecodegirl/loadgenerator:${env.BUILD_ID}").push()
                        docker.image("thecodegirl/loadgenerator:${env.BUILD_ID}").push('latest')
                    }
                }
            }
        }

        stage('Build paymentservice and push to dockerhub') {
            steps {
                script {
                    //build adservice
                    checkout scm
                    docker.build("thecodegirl/paymentservice:${env.BUILD_ID}", "-f /var/lib/jenkins/paymentservice/Dockerfile /var/lib/jenkins/paymentservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://hub.docker.com/', DOCKER_HUB_CREDENTIALS) {
                        docker.image("thecodegirl/paymentservice:${env.BUILD_ID}").push()
                        docker.image("thecodegirl/paymentservice:${env.BUILD_ID}").push('latest')
                    }
                }
            }
        }
        stage('Build productcatalogservice and push to dockerhub') {
            steps {
                script {
                    //build adservice
                    checkout scm
                    docker.build("thecodegirl/productcatalogservice:${env.BUILD_ID}", "-f /var/lib/jenkins/productcatalogservice/Dockerfile /var/lib/jenkins/productcatalogservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://hub.docker.com/', DOCKER_HUB_CREDENTIALS) {
                        docker.image("thecodegirl/productcatalogservice:${env.BUILD_ID}").push()
                        docker.image("thecodegirl/productcatalogservice:${env.BUILD_ID}").push('latest')
                    }
                }
            }
        }
        stage('Build recommendationservice and push to dockerhub') {
            steps {
                script {
                    //build adservice
                    checkout scm
                    docker.build("thecodegirl/recommendationservice:${env.BUILD_ID}", "-f /var/lib/jenkins/recommendationservice/Dockerfile /var/lib/jenkins/recommendationservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://hub.docker.com/', DOCKER_HUB_CREDENTIALS) {
                        docker.image("thecodegirl/recommendationservice:${env.BUILD_ID}").push()
                        docker.image("thecodegirl/recommendationservice:${env.BUILD_ID}").push('latest')
                    }
                }
            }
        }
        stage('Build shippingservice and push to dockerhub') {
            steps {
                script {
                    //build adservice
                    checkout scm
                    docker.build("thecodegirl/shippingservice:${env.BUILD_ID}", "-f /var/lib/jenkins/shippingservice/Dockerfile /var/lib/jenkins/shippingservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://hub.docker.com/', DOCKER_HUB_CREDENTIALS) {
                        docker.image("thecodegirl/shippingservice:${env.BUILD_ID}").push()
                        docker.image("thecodegirl/shippingservice:${env.BUILD_ID}").push('latest')
                    }
                }
            }
        }
        stage('Cleanup Local Docker Images') {
            steps {
                script {
                    def microservices = ['adservice', 'cartservice', 'checkoutservice', 'currencyservice', 'emailservice', 'frontend', 'loadgenerator', 'paymentservice', 'productcatalogservice', 'recommendationservice', 'shippingservice' ]
                    microservices.each { microserviceName ->
                        sh "docker rmi -f thecodegirl/${microserviceName}:${env.BUILD_ID}"
                        sh "docker rmi -f thecodegirl/${microserviceName}:latest"
                    }
                }
            }
        }
 
        stage('Deploy to Amazon EKS') {
            steps {
                script {
                    withCredentials([
                        string(credentialsId: aws-access-key-id, variable: AWS_ACCESS_KEY_ID),
                        string(credentialsId: aws-secret-access-key, variable: AWS_SECRET_ACCESS_KEY)
                    ]) {
                        sh "aws eks --region us-east-1 update-kubeconfig --name eks-cluster"
                        sh "kubectl apply -f ~/microservices-demo/release/kubernetes-manifests.yaml"
                    }
                }
            }
        }

        stage('Rollout Deployment') {
            steps {
                script {
                    def microservices = ['adservice', 'cartservice', 'checkoutservice', 'currencyservice', 'emailservice', 'frontend', 'loadgenerator', 'paymentservice', 'productcatalogservice', 'recommendationservice', 'shippingservice' ]

                    microservices.each { microserviceName ->
                        def kubeDeploymentName = "${microserviceName}-deployment"
                        def kubeAppLabel = "app=${microserviceName}"

                        kubeConfig = readFile("${HOME}/.kube/config")
                        sh """
                        echo '$kubeConfig' > kubeconfig.yaml
                        kubectl set image deployment/${kubeDeploymentName} ${kubeDeploymentName}=thecodegirl/${microserviceName}:${env.BUILD_ID}
                        kubectl rollout restart deployment/${kubeDeploymentName}
                        """
                    }
                }
            }
        }
    }
}
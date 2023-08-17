pipeline {
    agent any

    environment {
        DOCKER_HUB_CREDENTIALS = credentials('Docker_Hub_Access_Key')
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
                    docker.build("thecodegirl/adservice:${env.BUILD_ID}", "~/microservices-demo/src/adservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://index.docker.io/v1/', 'docker-hub-credentials') {
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
                    docker.build("thecodegirl/cartservice:${env.BUILD_ID}", "~/microservices-demo/src/cartservice/src")

                    //push to docker hub
                    
                    docker.withRegistry('https://index.docker.io/v1/', 'docker-hub-credentials') {
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
                    docker.build("thecodegirl/checkoutservice:${env.BUILD_ID}", "~/microservices-demo/src/checkoutservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://index.docker.io/v1/', 'docker-hub-credentials') {
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
                    docker.build("thecodegirl/currencyservice:${env.BUILD_ID}", "~/microservices-demo/src/currencyservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://index.docker.io/v1/', 'docker-hub-credentials') {
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
                    docker.build("thecodegirl/emailservice:${env.BUILD_ID}", "~/microservices-demo/src/emailservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://index.docker.io/v1/', 'docker-hub-credentials') {
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
                    docker.build("thecodegirl/frontend:${env.BUILD_ID}", "~/microservices-demo/src/frontend")

                    //push to docker hub
                    
                    docker.withRegistry('https://index.docker.io/v1/', 'docker-hub-credentials') {
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
                    docker.build("thecodegirl/loadgenerator:${env.BUILD_ID}", "~/microservices-demo/src/loadgenerator")

                    //push to docker hub
                    
                    docker.withRegistry('https://index.docker.io/v1/', 'docker-hub-credentials') {
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
                    docker.build("thecodegirl/paymentservice:${env.BUILD_ID}", "~/microservices-demo/src/paymentservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://index.docker.io/v1/', 'docker-hub-credentials') {
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
                    docker.build("thecodegirl/productcatalogservice:${env.BUILD_ID}", "~/microservices-demo/src/productcatalogservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://index.docker.io/v1/', 'docker-hub-credentials') {
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
                    docker.build("thecodegirl/recommendationservice:${env.BUILD_ID}", "~/microservices-demo/src/recommendationservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://index.docker.io/v1/', 'docker-hub-credentials') {
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
                    docker.build("thecodegirl/shippingservice:${env.BUILD_ID}", "~/microservices-demo/src/shippingservice")

                    //push to docker hub
                    
                    docker.withRegistry('https://index.docker.io/v1/', 'docker-hub-credentials') {
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
                        string(credentialsId: 'aws-access-key-id', variable: 'AWS_ACCESS_KEY_ID'),
                        string(credentialsId: 'aws-secret-access-key', variable: 'AWS_SECRET_ACCESS_KEY')
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
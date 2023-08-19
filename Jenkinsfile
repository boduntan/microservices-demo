@Library('github.com/releaseworks/jenkinslib') _
pipeline {
    agent any

    environment {
        DOCKER_HUB_CREDENTIALS = 'dockerid'
        AWS_ACCESS_KEY_ID = credentials('AWS_Access_Key')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_Secret_Key')
        DOCKER_HUB_CREDENTIALS_USERNAME = 'oduntanbola@gmail.com'
        //registry = "YourDockerhubAccount/YourRepository"
        //registryCredential = 'dockerhub_id'
        
    }
    stages {
        //stage('Login to Docker Hub') {
            //steps {
               // script {
                        //sh "echo ${DOCKER_HUB_CREDENTIALS} | docker login -u ${DOCKER_HUB_CREDENTIALS_USERNAME} --password-stdin"
                //}
            //}     	                      	  
        //}
        stage('Build adservice and push to dockerhub') {
            steps {
                script {
                    //build adservice
                    checkout scm
                    docker.build("thecodegirl/adservice:${env.BUILD_ID}", "-f /var/lib/jenkins/adservice/Dockerfile /var/lib/jenkins/adservice")
                    
                    docker.withRegistry('https://registry.hub.docker.com', DOCKER_HUB_CREDENTIALS) {
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
                    docker.build("thecodegirl/cartservice:${env.BUILD_ID}", "-f /var/lib/jenkins/cartservice/src/Dockerfile /var/lib/jenkins/cartservice/src")

                    //push to docker hub
                    
                    docker.withRegistry('https://registry.hub.docker.com', DOCKER_HUB_CREDENTIALS) {
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
                    docker.build("thecodegirl/checkoutservice:${env.BUILD_ID}", "-f /var/lib/jenkins/checkout/Dockerfile /var/lib/jenkins/checkout")

                    //push to docker hub
                    
                    docker.withRegistry('https://registry.hub.docker.com', DOCKER_HUB_CREDENTIALS) {
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
                    docker.build("thecodegirl/currencyservice:${env.BUILD_ID}", "-f /var/lib/jenkins/currency/Dockerfile /var/lib/jenkins/currency")

                    //push to docker hub
                    
                    docker.withRegistry('https://registry.hub.docker.com', DOCKER_HUB_CREDENTIALS) {
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
                    
                    docker.withRegistry('https://registry.hub.docker.com', DOCKER_HUB_CREDENTIALS) {
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
                    docker.build("thecodegirl/frontend:${env.BUILD_ID}", "-f /var/lib/jenkins/frontend/Dockerfile /var/lib/jenkins/frontend")

                    //push to docker hub
                    
                    docker.withRegistry('https://registry.hub.docker.com', DOCKER_HUB_CREDENTIALS) {
                        docker.image("thecodegirl/frontend:${env.BUILD_ID}").push()
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
                    
                    docker.withRegistry('https://registry.hub.docker.com', DOCKER_HUB_CREDENTIALS) {
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
                    
                    docker.withRegistry('https://registry.hub.docker.com', DOCKER_HUB_CREDENTIALS) {
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
                    
                    docker.withRegistry('https://registry.hub.docker.com', DOCKER_HUB_CREDENTIALS) {
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
                    
                    docker.withRegistry('https://registry.hub.docker.com', DOCKER_HUB_CREDENTIALS) {
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
                    
                    docker.withRegistry('https://registry.hub.docker.com', DOCKER_HUB_CREDENTIALS) {
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
                    withCredentials([[
                        $class: 'UsernamePasswordMultiBinding', credentialsId: 'aws-key', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY'
                        ]]) {
                        sh "aws eks --region us-east-1 update-kubeconfig --name eks-cluster"
                        sh "kubectl apply -f /var/lib/jenkins/kubernetes-manifests.yaml"
                    }
                }
            }
        }

        stage('Rollout Deployment') {
            steps {
                script {
                    def microservices = ['adservice', 'cartservice', 'checkoutservice', 'currencyservice', 'emailservice', 'frontend', 'loadgenerator', 'paymentservice', 'productcatalogservice', 'recommendationservice', 'shippingservice' ]

                    microservices.each { microserviceName ->
                        //def kubeDeploymentName = "${microserviceName}-deployment"
                        //def kubeAppLabel = "app=${microserviceName}"

                        kubeConfig = readFile("${HOME}/.kube/config")
                        sh """
                        echo 'Running kubectl command for ${microserviceName}'
                        echo 'Running kubectl command for ${kubeDeploymentName}'
                        echo '$kubeConfig' > kubeconfig.yaml
                        kubectl set image deployment/${microserviceName}-deployment ${microserviceName}-deployment=thecodegirl/${microserviceName}:${env.BUILD_ID}
                        kubectl rollout restart deployment/${microserviceName}-deployment
                        """
                    }
                }
            }
        }
    }
}

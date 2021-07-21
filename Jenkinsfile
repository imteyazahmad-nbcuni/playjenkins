pipeline {
    agent any
    stages {
        stage('Initialization') {
            steps{
               sh 'echo "hello Kubectl" '
            }
        }
         stage('Deploy App')
            {
                steps {
                    script{
                          kubernetesDeploy(configs: "helloworld.yml", kubeconfigId: "News-Kubeconfig")
                    }
                }
            }
         stage('Deploy Service')
            {
                steps{
                    script{
                     kubernetesDeploy(configs: "helloworld-service.yml", kubeconfigId: "News-Kubeconfig")
                    }
                }
            }        
    }
}

pipeline {
    agent any
    stages {
        stage('Initialization') {
            sh 'echo "hello Kubectl" '
        }
         stage('Deploy App')
            {
                kubernetesDeploy(configs: "helloworld.yml", kubeconfigId: "News-Kubeconfig")    
            }
         stage('Deploy Service')
            {
                kubernetesDeploy(configs: "helloworld-service.yml", kubeconfigId: "News-Kubeconfig")    
            }
        
    }
}

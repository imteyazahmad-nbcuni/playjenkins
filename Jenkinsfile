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
                          kubernetesDeploy(configs: "nginx-deployment.yaml", kubeconfigId: "News-Kubeconfig")
                    }
                }
            }        
    }
}

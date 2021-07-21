pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
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
}

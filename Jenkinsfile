def divisionsContainerAPI

pipeline {
    agent any
    stages {
        stage('Deploy to Kubernetes') {
            /* This builds the actual image; synonymous to
            * docker build on the command line */
            steps {
                kubernetesDeploy(kubeconfigId: 'rasnetics_kubernetes',
                    configs: 'prometheus-k8.yml',
                    enableConfigSubstitution: false
                )
            }
        }
    }
}
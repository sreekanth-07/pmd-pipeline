#######

pipeline {
    agent any
        stages {
	   stage('Install Helm and Lint') {
                 steps {
	                script {
	                    // Download and install Helm
	                    sh 'curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3'
	                    sh 'chmod 700 get_helm.sh'
	                    sh './get_helm.sh'
	                    sh "echo 'Helm installed successfully'"
	                   // Assuming Helm is now installed, proceed with Helm linting
			   //  sh "ls -ltrh deploy-pipeline"
			   //  sh "ls -ltrh  deploy-pipeline/templates"
			   //  // sh 'find . -type f -iname "*.yaml" -or -iname "*.yml" | xargs helm lint ${WORKSPACE}/deploy-pipeline/'
			   //  sh "helm lint ${WORKSPACE}/deploy-pipeline/"
	                   // sh "helm lint ${WORKSPACE}/deploy-pipeline/ --values ${WORKSPACE}/deploy-pipeline/values-cop-phase2-dev.yaml"
			   // sh "helm lint /home/jenkins/agent/workspace/tsb-applications/secure-customer-authentication/dev/microservices/tsb-cop2-fetch-name-details-test/deploy-pipeline/ --values /home/jenkins/agent/workspace/tsb-applications/secure-customer-authentication/dev/microservices/tsb-cop2-fetch-name-details-test/deploy-pipeline/values-cop-phase2-dev.yaml"
	                  }
                 }
           }
        }
}

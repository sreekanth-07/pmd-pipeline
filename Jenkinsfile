pipeline {
    agent any
        stages {
            stage('Access File') {
                steps {
                    script {
			 sh "pwd"   
                        // Clones the repository to the workspace
		        git url: "https://github.com/sreekanth-07/pmd.git"
                        // Read the content of the file
                        sh 'echo "inside gradle stage"'
                        sh "pwd"
                        def fileContent = readFile './sample.txt'
                        sh "pwd"
                        // Print the content
                        echo fileContent

                        //Replacing microservice and imagetag with latest version
                        sh """
                        sed -i "/aaa-bbb-ccc/d" sample.txt
                        cat sample.txt
                        echo "bbb-ccc-ddd:21-10-2023-09-14" >> sample.txt
                        cat sample.txt
                        """
                    }
                }
            }
            stage('slackSend'){
                steps {
                //def slackChannel = "pmd"
                    slackSend (channel: "#zipfileupload", color: '#00FF00', message: "PMD Scan started: Job '${1} [${2}]'")
                    withCredentials([string(credentialsId: 'token', variable: 'token')]) {
                        sh '''
                        echo $token
                        pwd
                        curl -F file=@sample.txt -F "initial_comment=Automation results" -F channels=#zipfileupload -H "Authorization: Bearer $token" https://slack.com/api/files.upload
                        '''
                    }
                }
            }
        }
}

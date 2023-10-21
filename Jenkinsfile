pipeline {
    agent any
        stages {
            stage('Access File') {
                steps {
                    script {
                        // Read the content of the file
                        sh 'echo "inside gradle stage"'
                        sh "pwd"
                        def fileContent = readFile './sample.txt'
                        sh "pwd"
                        // Print the content
                        echo fileContent

                        sh """
                        sed -i "/aaa-bbb-ccc/d" sample.txt
                        cat sample.txt
                        echo "bbb-ccc-ddd:21-10-2023-09-14" >> sample.txt
                        cat sample.txt
                        """
                    }
                }
            }
        }
}

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
                    }
                }
            }
        }
}

pipeline {
    agent any
    stages {
        stage('Read JSON and Set Environment') {
            steps {
                script {
                    // Read the file
                    def jsonString = readFile(file: './file.json')
                    
                    def jsonSlurper = new groovy.json.JsonSlurper()
                    def jsonData = jsonSlurper.parseText(jsonString)
                    
                    // Parse the JSON
                    echo "JSON Data: $jsonData"
                    
                    // Loop through JSON and set environment variables
                    jsonData.each { key, value ->
                        echo "Key: ${key}, Value: ${value}"
                        // Set each key-value pair as an environment variable
                        env["${key}"] = value.toString()
                    }
                    
                    // Print all environment variables
                    sh 'printenv'
                }
            }
        }
        
        // Optional: Another stage to verify the environment variables
        stage('Verify Environment Variables') {
            steps {
                script {
                    jsonData.each { key, value ->
                        echo "Env ${key}: ${env."${key}"}"
                    }
                }
            }
        }
    }
}

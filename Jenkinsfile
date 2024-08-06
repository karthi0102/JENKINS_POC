pipeline {
    agent any
    stages {
        stage('Read JSON') {
            steps {
                script {
                    // Read the file
                    def jsonString = readFile(file: './file.json')
                    
                    // Parse the JSON
                    def jsonSlurper = new groovy.json.JsonSlurper()
                    def jsonData = jsonSlurper.parseText(jsonString)
                    
                    // Now you can use the jsonData object
                  
                    
                    // If you have an array in your JSON
                    jsonData.items.each { item ->
                        echo "Item: ${item}"
                    }
                    
                    // If you need the entire JSON as a string again
                    def jsonBuilder = new groovy.json.JsonBuilder(jsonData)
                    def jsonOutput = jsonBuilder.toPrettyString()
                    echo "Full JSON: ${jsonOutput}"
                }
            }
        }
    }
}

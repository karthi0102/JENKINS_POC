pipeline {
    agent any
    stages {
        stage('Read JSON') {
            steps {
                script {
                    // Read the file
                    def jsonString = readFile(file: './file.json')

                    def jsonString = readFile(file: 'path/to/your/file.json')
def jsonSlurper = new groovy.json.JsonSlurper()
def jsonData = jsonSlurper.parseText(jsonString)
                    
                    // Parse the JSON
                      echo "$jsonData"
                   jsonData.each { key, value ->
    echo "Key: ${key}, Value: ${value}"
}
                    
                    // If you have an array in your JSON
                    
                    
                    // If you need the entire JSON as a string again
                   
                }
            }
        }
    }
}

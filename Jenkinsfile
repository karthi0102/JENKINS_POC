pipeline {
    agent any
    stages {
        stage('Read JSON') {
            steps {
                script {
                    // Read the file
                    def jsonString = readFile(file: './file.json')
                    
                    // Parse the JSON
                      echo "$jsonString"
                   jsonString.each { key, value ->
    echo "Key: ${key}, Value: ${value}"
}
                    
                    // If you have an array in your JSON
                    
                    
                    // If you need the entire JSON as a string again
                   
                }
            }
        }
    }
}

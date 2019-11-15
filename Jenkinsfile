pipeline {
    agent any
    stages {
        stage('SonarQube') {
            environment {
            scannerHome = tool 'sonar-scanner'
            }
            
            steps {
                    dir("./SimpleCustomerApp/") {
                        withSonarQubeEnv('SonarQube-Server') {                    
                        sh "${scannerHome}/bin/sonar-scanner"
                        }
                    }
            }
        
        
        }
    }
}
